# Historial de versiones

## Versión 2.0 — 2026-11-22

Rediseño integral de **Asistente de Tesis**.

### Nuevo
- Identidad visual renovada (azul marino, verde azulado y ámbar), logotipo propio y diseño adaptable a móviles.
- Ruta guiada de cinco pasos con indicador de avance: pregunta, diseño, revisión ética, tamaño muestral y plan de análisis.
- Módulo de pregunta de investigación (PECO, PICO, CoCoPop, PIRD, PFO, SPIDER) con criterios FINER y objetivo general.
- «Mi protocolo»: guardado automático en el navegador y exportación a Word, PDF o texto.
- Herramienta Verificador crítico EQUATOR: 13 diseños × 7 ítems críticos, integrada también en el resultado del diseño.
- Diseño del estudio: cualitativos, métodos mixtos, revisiones sistemáticas y de alcance, validación de instrumentos, modelos predictivos, ensayos de no inferioridad, cruzados y por conglomerados. Guías CONSORT 2025 y SPIRIT 2025, PRISMA 2020, TRIPOD+AI, COSMIN, COREQ y SRQR.
- Tamaño muestral: una media, casos y controles (OR), correlación, efecto de diseño (DEFF) a partir del coeficiente de correlación intraconglomerado (CCI), corrección de continuidad de Fleiss y párrafo de justificación para el protocolo.
- Plan de análisis: concordancia y fiabilidad (kappa, CCI, Bland–Altman, α y ω) y propósito del modelo multivariable (explicativo, predictivo o exploratorio).
- Calculadora 2×2: caso-control pareado (McNemar exacta), tasas por persona-tiempo (Byar, IRR), recálculo de VPP y VPN según probabilidad pretest y NNT al estilo de Altman.
- Funcionamiento sin conexión (archivo autocontenido y service worker instalable), botón para compartir y donación voluntaria en «Acerca de».

### Revisión ética rediseñada
- Flujo adaptativo según el tipo de estudio (datos públicos, uso secundario o contacto con participantes), sin preguntas repetidas ni irrelevantes.
- Opciones filtradas según las respuestas previas y detección de contradicciones (p. ej., consentimiento firmado en un instrumento anónimo; riesgo «mínimo» con procedimientos invasivos).
- La relación de dependencia con el investigador se trata como riesgo de coerción, no como vulnerabilidad.
- Resultado personalizado: nivel probable de revisión con sus motivos, aspectos que evaluará el CEI, documentación, elementos de la información al participante, asentimiento por edad, plan de manejo de datos y marco normativo.
- Marco normativo: Pautas éticas internacionales CIOMS/OPS (2016); Declaración de Helsinki (revisión de octubre de 2024); ICH E6(R3) (2025) para ensayos clínicos; OMS (2024) sobre IA en salud; en República Dominicana, CONABIOS, Ley 42-01, Ley 172-13 y Ley 136-03.

### Correcciones metodológicas
- Cohorte solo cuando la población inicial está libre del desenlace.
- Diferencias absolutas en puntos porcentuales; valores p menores de 0.001 expresados como «< 0.001».
- VPP y VPN no se calculan con muestreo de dos puertas; orientación uniforme de las tablas 2×2.
- Advertencia cuando la precisión absoluta es igual o mayor que la proporción esperada; efecto de diseño aplicado antes de la corrección por población finita.
- Corrección del botón de copia con apóstrofos, foco visible con teclado y desplazamiento al resultado en móviles.

## Versión 1.0 — 2026-09-14

Primera versión pública de **Asistente de Tesis**.

### Incluye
- Revisión ética.
- Diseño adaptativo del estudio.
- Selección adaptativa de análisis estadísticos.
- Análisis de tablas 2×2 según diseño epidemiológico.
- Cálculo de tamaño muestral.
- Intervalos de confianza del 95% cuando corresponde.
- Procesamiento local en el navegador.
- Sección “Acerca de” con autoría, ORCID, LinkedIn, alcance, privacidad, licencia, metodología y referencias.
