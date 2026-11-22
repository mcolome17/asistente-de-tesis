# Nota técnica — Asistente de Tesis v2.0

## Propósito
Herramienta educativa para apoyar decisiones metodológicas frecuentes en investigaciones de Ciencias de la Salud, desde la pregunta de investigación hasta el plan de análisis.

## Arquitectura
Aplicación autocontenida en un único archivo HTML con HTML, CSS y JavaScript, sin dependencias ni fuentes externas. Los cálculos se ejecutan localmente en el navegador y el avance se guarda en el almacenamiento local del navegador. Los archivos `sw.js` y `manifest.webmanifest` permiten instalarla y usarla sin conexión cuando se sirve por HTTPS.

## Métodos implementados
- Proporciones: intervalo de confianza del 95% mediante Wilson.
- Diferencias de proporciones o riesgos: método de Newcombe basado en Wilson, expresadas en puntos porcentuales.
- Razones epidemiológicas (RP, RR, OR, LR): intervalos de confianza del 95% por transformación logarítmica.
- Celdas cero: corrección de Haldane–Anscombe (0.5) solo cuando es necesaria para estimar razones e intervalos.
- OR pareado: cociente de pares discordantes con prueba de McNemar exacta (binomial bilateral).
- Tasas por persona-tiempo: intervalos de Byar para cada tasa y razón de tasas por transformación logarítmica.
- Asociación en tablas 2×2: χ² de Pearson, o prueba exacta de Fisher si alguna frecuencia esperada es menor de 5.
- VPP y VPN para otra probabilidad pretest: teorema de Bayes.
- NNT/NNH: inverso de la diferencia de riesgos; si su intervalo incluye 0, se informa con el formato de Altman (NNTB … a ∞ a NNTH …).
- Tamaño muestral: una proporción, una media, prevalencia con efecto de diseño (DEFF directo o DEFF = 1 + (m − 1)·CCI, aplicado antes de la corrección por población finita), dos proporciones (Fleiss, con corrección de continuidad opcional), casos y controles (p₁ = OR·p₀ / [1 + p₀(OR − 1)]), dos medias, correlación (transformación z de Fisher) y exactitud diagnóstica (Buderer).

## Guías de reporte
La aplicación orienta, según el diseño, hacia STROBE, CONSORT 2025 y SPIRIT 2025, TREND, STARD, CARE, PRISMA 2020, TRIPOD+AI, COSMIN, COREQ, SRQR y EQUATOR Network. El Verificador crítico EQUATOR resume 7 ítems críticos por diseño y no sustituye las listas oficiales completas.

## Revisión ética
Orientación preliminar basada en las Pautas éticas internacionales para la investigación relacionada con la salud con seres humanos (CIOMS/OPS, 2016), la Declaración de Helsinki de la AMM (revisión de octubre de 2024), la guía ICH E6(R3) de Buenas Prácticas Clínicas (adoptada el 6 de enero de 2025) para ensayos clínicos y la guía de la OMS sobre ética y gobernanza de la IA para la salud (2024). Para República Dominicana se consideran CONABIOS, la Ley 42-01 General de Salud, la Ley 172-13 de Protección de Datos Personales y la Ley 136-03. Las categorías de revisión (exención, expedita, completa) varían entre comités; la decisión corresponde siempre al Comité de Ética de Investigación.

## Referencias principales
- Wilson EB. Probable inference, the law of succession, and statistical inference. *Journal of the American Statistical Association*. 1927.
- Newcombe RG. Interval estimation for the difference between independent proportions: comparison of eleven methods. *Statistics in Medicine*. 1998.
- Fleiss JL, Levin B, Paik MC. *Statistical Methods for Rates and Proportions*. 3.ª ed. Wiley; 2003.
- Buderer NM. Statistical methodology: I. Incorporating the prevalence of disease into the sample size calculation for sensitivity and specificity. *Academic Emergency Medicine*. 1996.
- Altman DG. Confidence intervals for the number needed to treat. *BMJ*. 1998.
- Consejo de Organizaciones Internacionales de las Ciencias Médicas (CIOMS), Organización Panamericana de la Salud. *Pautas éticas internacionales para la investigación relacionada con la salud con seres humanos*. 4.ª ed. 2016.
- Asociación Médica Mundial. *Declaración de Helsinki: principios éticos para la investigación médica con participantes humanos*. Revisión de octubre de 2024.

## Estado de validación
La versión 2.0 fue sometida durante su desarrollo a pruebas funcionales de navegación, ramas adaptativas y escenarios de cálculo. Los cálculos principales se contrastaron con SciPy (Wilson, χ², Fisher, RR, OR y tamaños muestrales) y con valores de referencia publicados (Byar, McNemar exacta, Bayes). Esto no constituye una validación estadística externa independiente ni una certificación regulatoria.

Para usos científicos formales se recomienda contrastar los cálculos relevantes con software estadístico especializado y revisar las decisiones metodológicas con un profesional competente.

## Derechos de autor
© 2026 Manuel Colomé Hidalgo. Todos los derechos reservados.
