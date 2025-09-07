# Visual Development — Quick Visual Check (Amazon Q + Playwright MCP)

**Objetivo:** Validar visualmente cada cambio de front con evidencia y chequeos mínimos.

## Procedimiento inmediato post-cambio
1) **Identificar qué cambió** (componentes/vistas afectadas).
2) **Navegar a las vistas afectadas**  
   - Usá `mcp__playwright__browser_navigate` para cada ruta cambiada.
3) **Capturar evidencia**  
   - `mcp__playwright__browser_resize` a **1440×900** (desktop) y `mcp__playwright__browser_take_screenshot` (full page).
4) **Consola del navegador**  
   - `mcp__playwright__browser_console_messages` para errores/warnings.
5) **Cumplimiento de diseño**  
   - Comparar contra **[Principios de diseño](01-pricipios-de-diseño.md)**.
6) **Validar aceptación**  
   - Confirmar que el cambio cumple el pedido y criterios.

> Si hay tiempo, repetir screenshots en **768px** (tablet) y **375px** (mobile) y verificar que no haya scroll horizontal ni solapamientos.

## Formato mínimo del reporte
- **Resumen** (1–2 líneas)  
- **Evidencia** (screenshots por viewport)  
- **Hallazgos** con severidad: **[Blocker] / [High] / [Medium] / Nit:**  
- **Notas de aceptación** (qué requerimiento quedó cubierto)
