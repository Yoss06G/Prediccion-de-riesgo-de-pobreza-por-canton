# Predicción de Riesgo Socioeconómico por Cantón (Ecuador)

Este proyecto desarrolla un sistema predictivo para estimar el **Índice de Riesgo Socioeconómico (IRS)** a nivel cantonal en Ecuador, derivando el **Índice de Resiliencia Local (IRL)** como herramienta para la focalización de política pública y asignación presupuestaria por parte de los GAD Provinciales y el MIDESO.

## Metdología del Proyecto 

El proyecto se desarrollo usando la metdología ágil que consiste en dividir las fases del proyecto en 2 sprints:

### Sprint 1:
1. Obtención de datos y documentación de la fuente
2. Diccionario de datos con la información de cada una de las columnas
3. Dataset con los datos en crudo
4. Pipeline de limpieza documentado con el respectivo Exploratory Data Analysis
5. Dataset limpio exportado

### Sprint 2:

6. Modelos baseline y decisión de mejor modelo
7. Evaluación dual completa
8. Model Card completo
9. Checklist ético y LOPDP
10. Decision Log actualizado
11. Dashboard de reporte
12. Documentos Integrador

## Roles/profesionales involucrados

* Data Engineer - Kevin Delgado
* Data Analyst - Evelyn Oña
* Data Scientist - Yoslava Garófalo
* Machine Learning Engineer - Juan Ramos
* Data Steward - Alisson Manosalvas
  
## Descripción del Proyecto
Ecuador carece actualmente de métricas cantonales de riesgo socioeconómico entre censos, lo que dificulta la toma de decisiones basada en datos con horizonte predictivo. Este sistema utiliza registros administrativos oficiales (2019-2024) para proyectar el riesgo a 2025-2026.

*   **Alcance:** 219 cantones del Ecuador.
*   **Modelo Ganador:** TS2 - Autorregresivo AR(1) con Tendencia Lineal.
*   **KPI de Negocio:** Índice de Resiliencia Local (IRL) - Semáforo de intervención prioritaria.
*   **Cumplimiento LOPDP:** 8/12 principios plenos, 0 incumplidos.

## Resultados Clave
*   **Métricas de Desempeño (Test 2024):** 
    *   RMSE: `0.00351`
    *   R²: `0.9981`
*   **Semáforo IRL:** 
    *   🔴 `IRL ≤ 0`: Intervención Prioritaria
    *   🟡 `IRL ≈ 0`: Monitoreo
    *   🟢 `IRL > 0`: Resiliente

── docs/               # Model Card, Decision Log y Checklist LOPDP
├── src/                # Scripts de automatización y funciones auxiliares
└── README
