# -Hotel-Bookings-AI
Proyecto de reservas hoteleras usando un agente de IA corriendo completamente en local

El proyecto resolvió el análisis de un dataset real de 119,390 reservas hoteleras usando un agente de IA corriendo completamente en local. Se demostró que un modelo de 7B parámetros puede analizar datos con precisión cuando se configura correctamente: prompt con ejemplo ReAct explícito, DataFrame reducido a las columnas necesarias, y consultas técnicas con nombres exactos de columnas. El resultado es un flujo de análisis reproducible, sin costo de API y con privacidad total de los datos.

📌 Dataset
Hotel Booking Demand — Kaggle

# 🏨 Hotel Bookings — AI Data Analyst Local

Agente de análisis de datos en lenguaje natural usando LangChain + Ollama, sin API de pago, sin envío de datos a la nube.

---

## 🧠 Stack

| | |
|---|---|
| Lenguaje | Python 3.11 |
| Datos | pandas |
| Agente IA | LangChain Experimental |
| Modelo LLM | qwen2.5-coder:7b (Ollama local) |
| Entorno | Jupyter Notebook / VS Code |

---

## 📊 Resultados del Análisis

Dataset: `hotel_bookings.csv` — 119,390 reservas hoteleras (2015–2017)

| Métrica | Resultado |
|---|---|
| Total de reservas | 119,390 |
| Reservas canceladas | 44,224 — 37.04% |
| No-Show | 1,207 |
| ADR promedio City Hotel | €105.30 |
| ADR promedio Resort Hotel | €94.95 |
| Mes con más cancelaciones | Agosto |
| Segmento con más cancelaciones | Online TA |
| Customer type con mayor ADR | Transient |
| Mayor ADR por hotel + segmento | City Hotel — Direct |

---

## 🚀 Uso

```bash
# 1. Descargar modelo
ollama pull qwen2.5-coder:7b

# 2. Instalar dependencias
pip install langchain langchain-experimental langchain-ollama pandas

# 3. Abrir notebook y ejecutar celda por celda
```

Cada consulta va en una celda separada para controlar el resultado antes de continuar:

```python
agent.invoke("¿Cuántos registros tienen is_canceled igual a 1?")['output']
```
