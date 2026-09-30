# Marketing Digital, IA y Publicidad de Pago (2020–2025)

**Proyecto de Desarrollo · Parte 1**
**Estudiante:** Abella Thomas ([GitHub](https://github.com/thomasa39))

[![Sitio en Netlify](https://img.shields.io/badge/sitio-Netlify-00C7B7)](https://capable-taiyaki-9fb3d2.netlify.app/)
[![Licencia MIT](https://img.shields.io/badge/licencia-MIT-blue)](LICENSE)

---

## 1. Descripción General y Objetivo Académico

Este proyecto reúne un **informe final de investigación**, **dos planillas de Excel** con datos cuantitativos y una **página web de una sola página** que presenta los resultados. El tema es el análisis quinquenal (2020–2025/2026) de la transformación del marketing digital, la inteligencia artificial y la publicidad de pago.

**Objetivo general:** documentar cómo la pérdida de señales de seguimiento, la concentración del mercado y la IA generativa cambiaron la compra de medios, el costo de adquisición de clientes y la medición de resultados.

**Objetivos específicos**

- Cuantificar la inversión publicitaria digital global por canal entre 2020 y 2025.
- Comparar el rendimiento de Google Ads y Meta Ads (CTR, CPC, CPL y conversión).
- Explicar el marco regulatorio que afecta a las agencias, en particular el Reglamento de IA de la Unión Europea (UE 2024/1689).
- Presentar los hallazgos en un sitio web responsive con gráficos interactivos.

---

## 2. Justificación del Tema en Recursos Digitales y Marketing

- **Es un cambio estructural, no una moda.** Entre 2020 y 2025 el gasto digital global pasó de USD 433,5 mil millones a una estimación de USD 850 mil millones, y su peso sobre el total publicitario subió del 55 % al 75 % (estimado).
- **Afecta directamente a quien gestiona recursos digitales.** El CPC de Google Ads subió de USD 2,76 a USD 5,26, y el CPL de Meta Ads de USD 18,00 a USD 27,39. Gestionar presupuestos hoy exige entender estas alzas.
- **La IA cambió el trabajo creativo y operativo.** La adopción de IA en alguna función pasó del 15 % (estimado) al 88 %, y la creatividad se volvió la principal forma de segmentación.
- **La regulación ya está en marcha.** El etiquetado de contenido sintético (Art. 50 del Reglamento de IA) es obligatorio desde agosto de 2026 y las sanciones llegan al 3–7 % de la facturación global.
- **Conecta con la profesión.** El proyecto pone en práctica la gestión de recursos digitales: datos, herramientas de IA, medición y comunicación de resultados en la web.

---

## 3. Bitácora de Metodología

El flujo combinó tres herramientas, cada una con un rol distinto.

| Paso | Herramienta | Resultado |
|---|---|---|
| 1 | Perplexity | Búsqueda de datos cuantitativos con fuentes (tablas de búsqueda 1 y 2 del informe) |
| 2 | NotebookLM | Consolidación y síntesis del informe final sobre las fuentes cargadas |
| 3 | Claude | Diseño de las dos planillas de Excel con fórmulas |
| 4 | Claude | Construcción de la página web `index.html` |
| 5 | Claude | Redacción de este `README.md` |

### Paso 1 · Perplexity: búsqueda de datos

Objetivo: obtener estimaciones año a año (2020–2025) con fuentes verificables para cada Excel.


[[Hilo de Perplexity](https://www.perplexity.ai/search/d33f2d91-fdb9-4128-b844-781027bed234)]


### Paso 2 · NotebookLM: síntesis del informe

Objetivo: integrar las fuentes en el informe final (`INFORME_FINAL_DE_INVESTIGACIÓN.docx`). Las afirmaciones sin cita directa aparecen marcadas como `[Informe base]`.

[[NotebookLM](https://notebook.google.com/notebook/06d6dfb8-8090-4b58-b9a5-25005375e5fa>)]


### Paso 3 · Claude: diseño de los dos Excel

Prompt utilizado:

```text
Actúa como un analista de datos especializado en Recursos Digitales y Marketing. Con base en nuestro tema, necesito diseñar los datos numéricos completos para armar mis 2 archivos de Excel independientes. Proporcióname las tablas completas en formato de texto plano/Markdown estructurado para copiarlas a Excel:
1. EXCEL 1: [NOMBRE DEL EXCEL 1 SEGÚN EL TEMA] - Filas: Años de 2020 a 2025 (por categorías/canales). - Columnas: Año | Categoría/Canal | Métrica 1 | Métrica 2 | Métrica 3 | Métrica 4.
2. EXCEL 2: [NOMBRE DEL EXCEL 2 SEGÚN EL TEMA] - Filas: Años de 2020 a 2025 (por categorías/canales). - Columnas: Año | Categoría/Canal | Métrica A | Métrica B | Métrica C | Métrica D.
3. FÓRMULAS DE EXCEL: - Incluye 3 fórmulas de Excel en español (=PROMEDIO(), =SUMA(), variación %) indicando en qué celda aplicarlas.
Salida: .xlsx
```

Resultado: dos archivos `.xlsx` con hoja `Datos` y hoja `Notas`, y fórmulas recalculadas sin errores.

- **Excel 1:** inversión publicitaria digital global por canal (Search, Social Media, Display y otros, Total digital).
- **Excel 2:** benchmarks de Google Ads y Meta Ads (CTR, CPC, CPL y conversión clic→lead).

Fórmulas aplicadas:

| Archivo | Celda | Fórmula | Qué calcula |
|---|---|---|---|
| Excel 1 | I2 | `=PROMEDIO(C20:C25)` | Gasto medio anual del total digital |
| Excel 1 | I3 | `=SUMA(C2:C7)` | Gasto acumulado en Search 2020–2025 |
| Excel 1 | I4 | `=(C25-C20)/C20` | Variación % del total digital 2020→2025 |
| Excel 2 | I2 | `=PROMEDIO(E2:E7)` | CPL medio de Google Ads |
| Excel 2 | I3 | `=(D7-D2)/D2` | Variación % del CPC de Google Ads |
| Excel 2 | I4 | `=(E13-E8)/E8` | Variación % del CPL de Meta Ads |

### Paso 4 · Claude: página web

Prompt utilizado:

```text
Actúa como un Desarrollador Front-End Senior. Genera una página web profesional, moderna, responsive y en formato de archivo único `index.html` basada en mi proyecto final, incluyendo las planillas de Excel que acabamos de crear. REQUISITOS TÉCNICOS: 1. Output único: Todo el código dentro de un ÚNICO archivo `index.html`. 2. Tailwind CSS vía CDN y Chart.js vía CDN para gráficos interactivos. 3. Incluye todo el código funcional sin placeholders (""). ESTRUCTURA DEL SITIO WEB: 1. HERO SECTION: Título, subtítulo, resumen ejecutivo y tarjetas KPI. 2. MARCO TEÓRICO: Resumen de conceptos clave del Word. 3. DASHBOARD DE DATOS: 2 gráficos en Chart.js y tablas estilizadas de los Excels. 4. REGULACIÓN Y PRIVACIDAD / UX E IA. 5. CONCLUSIONES Y BOTONES DE DESCARGA (Google Drive). 6. FOOTER: Créditos, carrera y enlace a GitHub. Usa un diseño Dark Mode moderno.
```

---

## 4. Estructura de Documentos de Soporte (Google Drive) y Resumen de Auditoría

### Documentos de soporte

| Documento | Formato | Contenido |
|---|---|---|
| Informe final de investigación | `.docx` | Resumen ejecutivo, marco teórico, métricas, regulación, metodologías y conclusiones |
| Excel 1 · Inversión publicitaria digital 2020–2025 | `.xlsx` | 24 filas (4 canales × 6 años), 4 métricas y 3 fórmulas |
| Excel 2 · Benchmarks Google Ads y Meta Ads 2020–2025 | `.xlsx` | 12 filas (2 plataformas × 6 años), 4 métricas y 3 fórmulas |

### Resumen de auditoría

Se revisaron los datos de los Excel contra las tablas del informe.

**Verificaciones superadas**

- Las 53 fórmulas del Excel 1 y las 9 del Excel 2 se recalcularon sin errores.
- El crecimiento interanual calculado del total digital coincide con el del informe (31,2 %, 8,1 %, 10,6 %, 16,3 % y 7,5 %).
- Los valores de Total digital, Search, Social Media, Google Ads y Meta Ads son los del informe. Las cifras de 2025 son estimaciones del propio informe.

**Datos calculados o estimados (no provienen del informe)**

- «Display y otros canales» se calcula como Total − Search − Social.
- La conversión clic→lead de Meta Ads se calcula como CPC ÷ CPL.
- El share programático por canal (Search, Social y Display) es una estimación propia, calibrada para que el promedio ponderado coincida con el total del informe.

**Observaciones para revisar en el informe**

1. **Search 2024.** La serie salta de 210 a 316 mil millones (+50,5 %), por lo que «Display y otros» cae un 19,1 % ese año.
2. **Mobile 2024.** El texto dice «más de 400 mil millones» y «65,3 % del gasto digital», pero la tabla indica 495 mil millones, que equivale a un 62,6 % de 790,35.
3. **Valores repetidos.** El CPL de Google Ads 2026 (USD 66,69) es igual al de 2024, y el CPA de Meta Ads 2025 (USD 23,10) es igual al de 2024.
4. **Ventanas móviles.** Los datos de Google Ads cubren periodos de 12 meses (por ejemplo, abril 2023–marzo 2024), no años calendario.
5. **Cifras sin cita directa.** Varias cifras de los capítulos 3 y 4 están marcadas como `[Informe base]` y conviene respaldarlas con una fuente.

---

## 5. Estructura del Repositorio y Código Web

```text
Proyecto-de-Desarrollo-Parte-1/
├── index.html    # Sitio completo (HTML, CSS y JavaScript en un solo archivo)
├── README.md     # Este documento
└── LICENSE       # Licencia MIT
```

Los documentos de soporte (informe y Excel) se alojan en Google Drive (ver sección 6).

### Código web

- **Archivo único:** `index.html`, sin proceso de compilación.
- **Estilos:** [Tailwind CSS](https://tailwindcss.com/) por CDN, con una paleta oscura personalizada.
- **Gráficos:** [Chart.js 4](https://www.chartjs.org/) por CDN.
- **Tipografías:** Bricolage Grotesque (títulos) e IBM Plex Sans (texto), desde Google Fonts.
- **Datos:** constantes de JavaScript al inicio del bloque `<script>` (`T`, `S`, `SO`, `G`, `M`), que reproducen las dos planillas.

**Secciones de la página**

1. Hero con resumen ejecutivo y 4 tarjetas KPI.
2. Marco teórico y las tres eras de la compra de medios.
3. Dashboard de datos: gráfico de barras apiladas (Excel 1), gráfico de líneas (Excel 2) y dos tablas.
4. Regulación y privacidad, con línea de tiempo del Reglamento de IA.
5. UX, creatividad e IA.
6. Conclusiones y botones de descarga.
7. Footer con créditos y enlace a GitHub.

**Interactividad:** el gráfico 1 alterna entre gasto y participación, la tabla 1 se filtra por canal, el gráfico 2 cambia de métrica y la línea de tiempo marca cada hito como «En vigor» o «Próximo» según la fecha actual.

### Ejecutar en local

```bash
git clone https://github.com/thomasa39/Proyecto-de-Desarrollo-Parte-1.git
cd Proyecto-de-Desarrollo-Parte-1
# Abrir index.html con doble clic o desde un navegador
```

---

## 6. Enlaces del Proyecto

| Recurso | Enlace |
|---|---|
| Sitio web (Netlify) | https://capable-taiyaki-9fb3d2.netlify.app/ |
| Repositorio (GitHub) | https://github.com/thomasa39/Proyecto-de-Desarrollo-Parte-1 |
| Informe final (Google Drive) | https://drive.google.com/drive/folders/154osnY9avwKQzSNYm0Mdphk1HEnaiFAv?usp=drive_link |
| Excel 1 · Inversión digital (Google Drive) | https://drive.google.com/drive/folders/154osnY9avwKQzSNYm0Mdphk1HEnaiFAv?usp=drive_link |
| Excel 2 · Google y Meta Ads (Google Drive) | https://drive.google.com/drive/folders/154osnY9avwKQzSNYm0Mdphk1HEnaiFAv?usp=drive_link |

---

## Licencia

Distribuido bajo licencia MIT. Consulta el archivo [LICENSE](LICENSE).
