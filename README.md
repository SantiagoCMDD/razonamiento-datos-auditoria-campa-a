# Una base de datos, muchas historias

**Auditoría de una afirmación con datos — Campaña de acompañamiento académico, Universidad Horizonte**

Asignatura: Razonamiento con Datos
Lectura aplicada: Silver, N. (2012). *The Signal and the Noise*, capítulos 1 y 2.

| Rol | Integrante |
|---|---|
| Narrador de datos | Santiago Parada |
| Auditor de evidencia | Santiago Parada |
| Auditor visual | Francisco Castro |

---

## La afirmación auditada

> *"La campaña transformó el desempeño estudiantil: aumentó la participación, mejoró las notas y redujo el abandono."*

## Veredicto

**`NO PUBLICABLE`**

Una de las tres afirmaciones es falsa en los propios datos de la universidad, y las otras dos descansan sobre una comparación inválida entre grupos que nunca fueron comparables.

---

## Contenido del repositorio

| Archivo | Qué es |
|---|---|
| [`auditoria_campana.ipynb`](auditoria_campana.ipynb) | Análisis completo y reproducible. **Se lee directamente en GitHub.** |
| [`presentacion_auditoria.pptx`](presentacion_auditoria.pptx) | Presentación de 14 diapositivas (descargar para ver) |
| [`presentacion_auditoria.pdf`](presentacion_auditoria.pdf) | La misma presentación, visible en el navegador |

## Cómo leer el trabajo

El notebook sigue una lógica deliberada: primero demuestra que la misma base sostiene dos relatos opuestos, y solo después explica por qué.

| Sección | Contenido |
|---|---|
| 1–2 | Datos, diccionario de variables y confrontación del mensaje con las cifras |
| 3 | **Historia A** — pieza persuasiva (gráficos deliberadamente engañosos) |
| 4 | **Historia B** — pieza crítica, con autocrítica de sus propios sesgos |
| 5 | Auditoría comparativa: 8 hallazgos con evidencia numérica |
| 6 | **Versión final ética** — la que sí recomendaríamos publicar |
| 7 | Tres ideas de Silver aplicadas al caso |
| 8 | Limitaciones de nuestra propia auditoría |
| 9–10 | Veredicto, recomendación y referencias |

> **Advertencia:** los gráficos de la sección 3 son engañosos a propósito. Ninguna cifra fue inventada ni modificada en ninguna parte del trabajo: toda la distorsión proviene de decisiones de selección, agregación, escala y lenguaje.

## Hallazgos principales

1. **Los grupos no eran comparables.** En los 12 de 12 programas, sin excepción, el grupo de alta exposición partía con peor nota previa. Bajo exposición independiente del nivel previo, ese patrón tendría probabilidad ≈ 1 en 4.096.
2. **Regresión a la media.** La correlación entre nota previa y magnitud del cambio es −0.72, y se mantiene *dentro* de cada grupo por separado (−0.88 y −0.76), donde la campaña no puede explicarla.
3. **La afirmación sobre abandono es falsa.** 6.25 % en exposición alta frente a 6.26 % en baja: una centésima de punto porcentual.

## Reproducibilidad

Ejecutar todas las celdas del notebook en orden reproduce la totalidad de las cifras y gráficos. Dependencias: `pandas`, `numpy`, `matplotlib`.

```bash
pip install pandas numpy matplotlib
jupyter notebook auditoria_campana.ipynb
```

## Referencias

Silver, N. (2012). *The Signal and the Noise: Why So Many Predictions Fail—but Some Don't*. Penguin Press. Capítulos 1 y 2.

Universidad Horizonte (2026). *Base de resultados de la campaña de acompañamiento académico por programa y nivel de exposición*. Documento interno entregado para la auditoría.
