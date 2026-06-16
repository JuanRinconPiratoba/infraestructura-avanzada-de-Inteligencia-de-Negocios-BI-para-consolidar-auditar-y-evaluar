# Simulación Avanzada de Portafolio Analítico: E-Commerce B2C 📊✨

## 📋 Descripción del Proyecto
Este proyecto implementa una infraestructura avanzada de Inteligencia de Negocios (BI) para consolidar, auditar y evaluar los resultados operacionales, comerciales y de marketing de una plataforma de comercio electrónico B2C. 

A través del motor de almacenamiento **VertiPaq** y un enfoque riguroso de ingeniería de datos, se resolvió la dispersión de datos y se unificaron las fuentes en un único repositorio de verdad, automatizando el cálculo de KPIs financieros y métricas de adquisición de clientes.

## 🛠️ Framework Técnico & Herramientas
* **Motor Analítico:** Excel Avanzado & Power Pivot (Motor VertiPaq).
* **Modelado de Datos:** Arquitectura en Estrella (Star Schema) con relaciones 1:N validadas.
* **Lenguaje de Consultas / Cálculos:** DAX Estructurado (Data Analysis Expressions).
* **Componentes Clave:** Tabla puente (`Dim_Tiempo`) para control de granularidad y consistencia temporal.

---

## 📐 Arquitectura de Datos e Ingeniería Solucionada

Uno de los mayores desafíos del proyecto fue el rediseño radical de la arquitectura de la base de datos debido a dos anomalías críticas identificadas durante la fase de auditoría:

1. **Resolución de Granularidad Mixta:** Las transacciones de la tabla de hechos (`Fact_Ventas`) registraban eventos a nivel diario, mientras que las asignaciones presupuestales de costos fijos operaban de forma agregada a nivel trimestral. Esto generaba un error de sobre-conteo sistemático en DAX, duplicando los montos y distorsionando el EBITDA. Se solucionó homologando la arquitectura a nivel mensual mediante la implementación de una tabla puente (`Dim_Tiempo`).
2. **Sincronización del Motor de Tiempo:** Se detectó un truncamiento en la dimensión calendario original y un desalineamiento donde ciertos gastos operativos aparecían cargados al año fiscal posterior (2026). Se expandió el motor a una dimensión calendario continua de 365 días y se homologaron las llaves fiscales al año en curso de la operación (2025), garantizando precisión absoluta en el cálculo del EBITDA indexado.

---

## 📈 KPIs y Resultados de Negocio Clave

* **Ingresos Totales Brutos:** \$26,095 USD
* **EBITDA Consolidado:** \$2,533 USD
* **Margen Neto Operacional:** 9.71% (Altamente competitivo para el sector retail e-commerce).
* **Eficiencia de Adquisición (LTV/CAC):** 7.83x (Superando ampliamente el estándar de la industria de 3.0x).

### 🛒 Rendimiento Comercial por Categoría
* **Tecnología:** Líder indiscutible en volumen de facturación y tasa de conversión de ganancia bruta.
* **Moda y Hogar:** Comportamiento financiero balanceado, rotación constante y sostén del flujo de caja.
* **Deportes:** Categoría de nicho. Baja facturación pero con un retorno porcentual unitario muy atractivo.

### 📣 Eficiencia de Canales de Marketing
* **Facebook Ads & Influencers:** Máxima retención y valor de vida del cliente (LTV elevado).
* **Orgánico (SEO/Directo):** CAC de \$0.00 USD, lo que empuja el ROI conceptualmente al infinito e inyecta margen limpio.
* **Google Ads:** Comportamiento lineal y predictivo, ideal para estabilizar proyecciones.

---

## 🚀 Recomendaciones Estratégicas Implementadas
* **Marketing:** Reasignación presupuestaria inmediata (incremento del 15% a Facebook Ads e Influencers) y blindaje de la estrategia SEO.
* **Comercial:** Asegurar stock en Tecnología y diseñar una estrategia de *cross-selling* (empaquetado) para la categoría Deportes junto a artículos de alta rotación de Hogar y Moda.
* **Gobernanza de Datos:** Establecer como política que cualquier métrica nueva respete el modelo en estrella implementado para evitar futuras duplicidades.
