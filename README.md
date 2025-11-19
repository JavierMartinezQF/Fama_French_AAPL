# Fama_French_AAPL
Implementación de modelo de Fama-French a AAPL 2015-2025


# 📈 Modelo de Fama-French aplicado a AAPL (2015–2025)

Este proyecto implementa un análisis cuantitativo del rendimiento de la acción **Apple Inc. (AAPL)** utilizando el modelo clásico de **3 factores de Fama-French**:

- **Mkt-RF**: Prima de mercado  
- **SMB**: Small Minus Big (tamaño)  
- **HML**: High Minus Low (valor)

El objetivo es evaluar qué tan bien estos factores explican el rendimiento en exceso de AAPL durante el periodo 2015–2025 y visualizar los resultados de forma clara.

---

## 🚀 Objetivos del proyecto

1. Descargar y explorar los **factores de Fama-French (diarios)** desde `pandas_datareader`.
2. Descargar precios y rendimientos de AAPL usando `yfinance`.
3. Construir rendimientos logarítmicos.
4. Calcular el **rendimiento en exceso** de AAPL sobre la tasa libre de riesgo.
5. Ajustar el modelo:

\[
R_{AAPL} - R_f = \alpha + \beta_{Mkt} (Mkt-RF) 
+ \beta_{SMB} SMB + \beta_{HML} HML + \varepsilon
\]

6. Visualizar:
   - Precios y rendimientos de AAPL
   - Comportamiento de los factores Fama-French
   - Matriz de correlación
   - Gráfica de dispersión: Mkt-RF vs rendimiento en exceso
   - Serie: rendimiento observado vs predicho
   - Residuales del modelo

7. Interpretar los factores y el alpha.

---

## 📦 Librerías utilizadas

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `statsmodels`
- `yfinance`
- `pandas_datareader`

---

## 📊 Resultados principales

### ✔️ 1. Alpha (constante)
- Muy cercano a **0**  
- **No significativo** estadísticamente  
- Implica que AAPL **no genera rendimiento extra** más allá de los factores

### ✔️ 2. Exposición al mercado (Mkt-RF)
- **β ≈ 1.16**  
- Altamente significativo  
- AAPL es más sensible que el mercado: ≈16% más volátil

### ✔️ 3. SMB
- **β negativo**  
- AAPL se comporta claramente como **empresa grande (large cap)**

### ✔️ 4. HML
- **β negativo**  
- AAPL tiene características de **acción de crecimiento (growth)**  
  — bajo book-to-market, tecnología, alto CAPEX

### ✔️ 5. Predicción vs observación
El modelo captura bien los movimientos de los rendimientos en exceso, con residuales centrados en cero y sin patrones claros.

---

## 📂 Estructura del notebook

Introducción

Descarga de factores Fama-French

Descarga de AAPL

Rendimientos y exploración

Correlaciones

Construcción del modelo

Visualizaciones cuantitativas

Conclusiones


---

## 📘 Conclusiones del análisis

- El modelo de Fama-French **explica adecuadamente** el comportamiento de AAPL.
- El rendimiento adicional (“alpha”) es prácticamente cero.
- AAPL sigue siendo un activo:
  - altamente dependiente del mercado,
  - con comportamiento típico de una gran tecnológica de crecimiento,
  - y sin evidencia estadística de rendimiento anormal.

Este análisis demuestra cómo aplicar modelos clásicos de finanzas cuantitativas a datos reales con Python.

---

## 🔧 Mejoras futuras (roadmap)

- Usar el **modelo de 5 factores** de Fama-French:
  - MOM (momentum)
  - RMW (profitability)
  - CMA (investment)
- Calcular **betas móviles** (rolling betas).
- Implementar **bootstrap de alpha**.
- Comparar AAPL contra:
  - MSFT  
  - NVDA  
  - AMZN  
  - SPY
- Reproducir el estudio en periodos más cortos y durante crisis.

---

## 📬 Contacto / Créditos

Proyecto desarrollado como parte del portafolio cuantitativo de **Javier Martínez** para análisis financiero con Python.


