# 🚢 Análisis de Supervivencia del Titanic

> 📊 Proyecto de análisis y visualización de datos utilizando **Python, Pandas, Matplotlib y Seaborn**.

---

## 📌 Descripción del proyecto

Este proyecto realiza un análisis exploratorio de los datos de los pasajeros del **Titanic**, con el propósito de identificar diferentes patrones relacionados con la supervivencia.

Se estudian variables como:

- 👤 Sexo
- 🎟️ Clase del pasajero
- 🎂 Edad
- 👨‍👩‍👧‍👦 Acompañamiento familiar
- 💰 Tarifa pagada
- ⚓ Puerto de embarque

El análisis incluye un proceso de **limpieza, transformación, análisis y visualización de los datos**.

---

# 📊 Dataset

### 📝 Nombre
**Titanic - Train Dataset (`train.csv`)**

### 📂 Fuente
El dataset utilizado se encuentra en:

```text
data/train.csv
```

### 📖 Descripción

El conjunto de datos contiene información de **891 pasajeros** y **12 variables iniciales**.

| Variable | Descripción |
|---|---|
| `PassengerId` | Identificador del pasajero |
| `Survived` | Supervivencia: 0 = No, 1 = Sí |
| `Pclass` | Clase del pasajero |
| `Name` | Nombre del pasajero |
| `Sex` | Sexo |
| `Age` | Edad |
| `SibSp` | Hermanos o cónyuges a bordo |
| `Parch` | Padres o hijos a bordo |
| `Ticket` | Número de boleto |
| `Fare` | Tarifa pagada |
| `Cabin` | Número de cabina |
| `Embarked` | Puerto de embarque |

---

# 🎯 Objetivo

El objetivo principal es analizar cómo distintas características de los pasajeros se relacionan con su supervivencia.

### ❓ Preguntas principales

**1.-** ¿Qué porcentaje de pasajeros sobrevivió?

**2.-** ¿Cómo cambia la supervivencia entre hombres y mujeres?

**3.-** ¿Cómo cambia la supervivencia según la clase del pasajero?

**4.-** ¿Qué grupos de edad presentan mayor supervivencia?

**5.-** ¿Viajar solo o acompañado parece estar relacionado con la supervivencia?

**6.-** ¿Existe alguna relación entre la tarifa pagada y la supervivencia?

---

# 🧹 Procesamiento de datos

Durante la exploración inicial se encontraron:

- 📋 **891 registros**
- 📊 **12 columnas**
- ✅ **0 registros duplicados**
- ⚠️ **177 valores faltantes en `Age`**
- ⚠️ **687 valores faltantes en `Cabin`**
- ⚠️ **2 valores faltantes en `Embarked`**

### 🔧 Tratamiento de valores faltantes

| Variable | Tratamiento |
|---|---|
| `Age` | Se reemplazaron los valores faltantes utilizando la mediana |
| `Embarked` | Se reemplazaron utilizando la moda |
| `Cabin` | Se reemplazaron por `"Desconocido"` |

### 🆕 Nuevas variables

Para mejorar el análisis se crearon tres variables adicionales:

| Variable | Descripción |
|---|---|
| `FamilySize` | Tamaño de la familia (`SibSp + Parch + 1`) |
| `IsAlone` | 1 = viajaba solo, 0 = acompañado |
| `AgeGroup` | Clasificación por grupo de edad |

Los grupos utilizados para `AgeGroup` son:

```text
Niño
Joven
Adulto
Adulto mayor
```

---

# 📈 Análisis y resultados

## 1️⃣ Supervivencia general

La supervivencia general fue:

> 🟢 **38.38%**

Es decir, **342 de 891 pasajeros** sobrevivieron.

---

## 2️⃣ Supervivencia por sexo

| Sexo | Tasa de supervivencia |
|---|---:|
| 👩 Mujeres | **74.20%** |
| 👨 Hombres | **18.89%** |

---

## 3️⃣ Supervivencia por clase

| Clase | Tasa de supervivencia |
|---|---:|
| 🥇 1ª Clase | **62.96%** |
| 🥈 2ª Clase | **47.28%** |
| 🥉 3ª Clase | **24.24%** |

---

## 4️⃣ Supervivencia por edad

| Grupo de edad | Tasa de supervivencia |
|---|---:|
| 🧒 Niño | **57.35%** |
| 🧑 Joven | **48.89%** |
| 🧔 Adulto | **36.44%** |
| 👴 Adulto mayor | **26.92%** |

---

## 5️⃣ Viajar solo vs. acompañado

| Situación | Tasa de supervivencia |
|---|---:|
| 👨‍👩‍👧 Acompañado | **50.56%** |
| 👤 Solo | **30.35%** |

---

## 6️⃣ Tarifa y supervivencia

| Resultado | Tarifa promedio |
|---|---:|
| ✅ Sobrevivió | **$48.40** |
| ❌ No sobrevivió | **$22.12** |

---

# 📊 Visualizaciones

El proyecto genera **6 gráficas** para representar los resultados:

| # | Gráfica |
|---|---|
| 1️⃣ | 📊 Porcentaje de supervivencia general |
| 2️⃣ | 👥 Supervivencia por género |
| 3️⃣ | 🎟️ Supervivencia por clase |
| 4️⃣ | 🎂 Supervivencia por grupo de edad |
| 5️⃣ | 👨‍👩‍👧 Supervivencia según acompañamiento |
| 6️⃣ | 💰 Distribución de tarifa según supervivencia |

Las gráficas se almacenan en:

```text
outputs/resultados/
```

---

# 💡 Conclusiones

A partir del análisis realizado se pueden observar diferencias en las tasas de supervivencia de acuerdo con las características de los pasajeros.

Entre los principales resultados se encuentran:

- 📌 La supervivencia general fue de **38.38%**.
- 👥 Se observaron diferencias en la supervivencia entre hombres y mujeres.
- 🎟️ La tasa de supervivencia varió según la clase del pasajero.
- 🎂 Los diferentes grupos de edad presentaron distintas tasas de supervivencia.
- 👨‍👩‍👧 Los pasajeros acompañados tuvieron una tasa de supervivencia diferente a quienes viajaban solos.
- 💰 La tarifa promedio fue diferente entre quienes sobrevivieron y quienes no.

---

# 🛠️ Tecnologías utilizadas

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-blue)

---

# 📦 Requisitos

Para ejecutar el proyecto necesitas:

- 🐍 Python 3.x
- 🐼 Pandas
- 📈 Matplotlib
- 📊 Seaborn

Las dependencias se encuentran especificadas en:

```text
requirements.txt
```

---

# 🚀 Instalación

## 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/Tadand-64/Titanic.git
```

## 2️⃣ Entrar al proyecto

```bash
cd Titanic
```

## 3️⃣ Crear el entorno virtual

```bash
python -m venv .venv
```

## 4️⃣ Activar el entorno virtual

### 🪟 Windows

```bash
.venv\Scripts\activate
```

### 🍎 macOS / 🐧 Linux

```bash
source .venv/bin/activate
```

## 5️⃣ Instalar las dependencias

```bash
pip install -r requirements.txt
```

---

# ▶️ Ejecución

Para ejecutar el análisis:

```bash
jupyter notebook src/analysis.ipynb
```

El programa utiliza:

```text
data/train.csv
```

y genera los resultados en:

```text
outputs/resultados/
```

---

# 📁 Estructura del proyecto

```text
📦 Titanic
│
├── 📂 data
│   └── 📄 train.csv
│
├── 📂 src
│   └── 📓 analysis.ipynb
│
├── 📂 outputs
│   └── 📂 resultados
│       ├── 📊 1_supervivencia_general.png
│       ├── 📊 2_supervivencia_genero.png
│       ├── 📊 3_supervivencia_clase.png
│       ├── 📊 4_supervivencia_edad.png
│       ├── 📊 5_supervivencia_acompanado.png
│       ├── 📊 6_supervivencia_tarifa.png
│       └── 📝 conclusiones.txt
│
├── 📄 .gitignore
├── 📄 requirements.txt
└── 📄 README.md
```