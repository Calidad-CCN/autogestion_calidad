# Dashboard de Calidad en Terreno · Clínica Cruz Nacional

Herramienta interna de uso exclusivo del **Área Clínica y Calidad** de Clínica Cruz Nacional.

## Archivos

| Archivo | Descripción |
|---|---|
| `index.html` | Dashboard principal de auditoría — uso del equipo de calidad en visitas a sucursales |
| `autogest.html` | Herramienta de autogestión — uso semanal de Gerentes de Sucursal |

---

## Dashboard principal (`index.html`)

Checklist de auditoría en terreno. Incluye:
- Checklist por áreas con semaforización (Óptimo / Medio / Bajo)
- Indicadores KPI por sucursal
- Gráficos: gauge, radar, ranking, tendencia, barras por área
- Fotos por área (hasta 5, comprimidas)
- Informe PDF completo con gráficos y fotos
- Plan de Acción en Word (.docx) editable con hallazgos del informe
- Historial de visitas con bloqueo de edición a 30 días
- Migración automática de versiones anteriores

**Almacenamiento:** `localStorage` (datos) + `IndexedDB` (fotos)  
**Storage key:** `cn_data_v4`

---

## Herramienta de autogestión (`autogest.html`)

Autoevaluación semanal para Gerentes de Sucursal. Incluye:
- Mismo checklist de 19 áreas y 195 ítems que el dashboard de auditoría
- Estados: ✅ Cumple / ❌ No cumple / 🔄 En gestión (con a quién, cuándo y por qué medio) / N/A
- Fotos de evidencia por área (hasta 5, comprimidas a 800×600 JPEG)
- Informe HTML completo con fotos incrustadas — se descarga directamente
- Historial de informes guardados en el dispositivo (visualización + descarga, sin edición)
- **Sin guardado de datos crudos** — solo el informe final queda guardado

**Almacenamiento:** `IndexedDB` (solo informes ya generados, sin localStorage)  
**Compatible con:** Chrome, Edge, Safari, Firefox modernos

---

## Uso

Abrir directamente en el navegador. No requiere servidor ni instalación.

El historial se guarda localmente en cada dispositivo — no se sincroniza entre dispositivos.

---

*Uso interno · Clínica Cruz Nacional SpA · Área Clínica y Calidad*
