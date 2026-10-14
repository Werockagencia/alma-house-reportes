# Alma House · Reportes de marketing

Cliente: **Alma House Nails Bar**, CC Montaña Plaza, local 4 · Cajicá · Agencia: We Rock
Cuentas: Ads Manager `1098029103168998` · Business Suite `1362311972781163` · IG `@almahouse.nails`

## Cadencia: mensual (corte a mitad de mes)
| Corte | Período | Carpeta |
|---|---|---|
| 14 oct 2026 | Sep 15 – Oct 14 (Nº 01) | `reportes/2026-10-14/` |
| **14 nov 2026** | Oct 15 – Nov 14 (Nº 02) | `reportes/2026-11-14/` (siguiente) |

En vivo: https://werockagencia.github.io/alma-house-reportes/

## Proceso de cada corte
1. **Pauta (Ads Manager)**, nivel campaña y anuncio, rango del corte, columnas *Rendimiento y clics*
   (resultados, alcance, frecuencia, costo/resultado, gasto, impresiones, CPM, clics al enlace, CTR, visitas a la página de destino)
   + rankings de calidad a nivel anuncio. Guardar en `data/AAAA-MM-DD_campanas.csv`.
2. **Orgánico (Business Suite → Estadísticas)**:
   - *Resultados* con plataforma = Instagram: visualizaciones, alcance, interacciones, clics al enlace, visitas al perfil, seguidores (series diarias).
   - *Contenido*: columnas Alcance, Visualizaciones, Interacciones, Comentarios, Guardados, Respuestas → `data/AAAA-MM-DD_contenidos_ig.csv`.
   - Seguidores totales desde el Inicio de Business Suite.
3. **Pedir a Alma House**: cuántas conversaciones de WhatsApp terminaron en cita y postulaciones recibidas.
4. Agregar la fila del mes a `data/historico_mensual.csv`.
5. Copiar `reportes/<último>/index.html` a la nueva carpeta, actualizar cifras y exportar el PDF:
   ```bash
   "/c/Program Files/Google/Chrome/Application/chrome.exe" --headless=new --no-pdf-header-footer --allow-file-access-from-files --virtual-time-budget=8000 --print-to-pdf="<ruta absoluta>/reportes/<fecha>/AlmaHouse_Reporte_<fecha>.pdf" "file:///<ruta absoluta>/reportes/<fecha>/index.html"
   ```
   (La ruta del PDF debe ser absoluta; con relativa Chrome no escribe el archivo.)

## Reglas de marca en los reportes
- Tipografías oficiales (Aurora Magnolia Serif + Uncage, Figtree para lectura) y paleta del manual.
- Hablar de "momento", nunca de "hora". Reels = producción audiovisual; We Rock entrega piezas estáticas.

## Estructura
```
assets/fonts, logos   tipografías y logos de marca
data/                 exports de Meta e histórico mensual
reportes/AAAA-MM-DD/  index.html + PDF de cada corte
index.html            índice de reportes
```
