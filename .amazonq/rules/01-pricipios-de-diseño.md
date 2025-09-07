# Checklist de diseño de dashboard SaaS de nivel S (inspirado en Stripe, Airbnb, Linear)

## I. Filosofía y estrategia de diseño

* [ ] **Usuarios primero:** priorizá necesidades, flujos y facilidad de uso en cada decisión de diseño.
* [ ] **Oficio meticuloso:** apuntá a precisión, pulido y alta calidad en cada elemento e interacción.
* [ ] **Velocidad y rendimiento:** diseñá para cargas rápidas e interacciones ágiles y responsivas.
* [ ] **Simplicidad y claridad:** buscá una interfaz limpia y sin desorden. Asegurá etiquetas, instrucciones e información inequívocas.
* [ ] **Foco y eficiencia:** ayudá a que las personas logren sus objetivos rápido y con mínima fricción. Reducí pasos o distracciones innecesarias.
* [ ] **Consistencia:** mantené un lenguaje de diseño uniforme (colores, tipografía, componentes, patrones) en todo el dashboard.
* [ ] **Accesibilidad (WCAG AA+):** diseñá para la inclusión. Asegurá contraste suficiente, navegación por teclado y compatibilidad con lectores de pantalla.
* [ ] **Diseño con opinión (predeterminados pensados):** establecé flujos y ajustes por defecto claros y eficientes, reduciendo la fatiga de decisión.

## II. Fundamentos del sistema de diseño (tokens y componentes base)

* [ ] **Definir una paleta de color:**

  * [ ] **Color de marca primario:** definido por el producto, usado estratégicamente.
  * [ ] **Neutros:** escala de grises (5–7 pasos) para texto, fondos y bordes.
  * [ ] **Colores semánticos:** definí colores específicos para Éxito (verde), Error/Destructivo (rojo), Advertencia (amarillo/ámbar) e Informativo (azul).
  * [ ] **Paleta para modo oscuro:** creá una paleta accesible equivalente para dark mode.
  * [ ] **Chequeo de accesibilidad:** asegurá que todas las combinaciones cumplan contraste WCAG AA.
* [ ] **Establecer una escala tipográfica:**

  * [ ] **Familia tipográfica principal:** elegí una sans-serif limpia y legible (p. ej., Inter, Manrope, system-ui).
  * [ ] **Escala modular:** definí tamaños para H1, H2, H3, H4, Cuerpo grande, Cuerpo medio (por defecto), Cuerpo pequeño/epígrafe (p. ej., H1: 32 px; Cuerpo: 14 px/16 px).
  * [ ] **Pesos tipográficos:** usá un set acotado (Regular, Medium, SemiBold, Bold).
  * [ ] **Interlineado:** asegurá interlineado generoso para legibilidad (p. ej., 1.5–1.7 en texto de cuerpo).
* [ ] **Definir unidades de espaciado:**

  * [ ] **Unidad base:** establecé una unidad (p. ej., 8 px).
  * [ ] **Escala de espaciado:** usá múltiplos de la base para padding, márgenes y layout (p. ej., 4, 8, 12, 16, 24, 32 px).
* [ ] **Definir radios de borde:**

  * [ ] **Valores consistentes:** usá un pequeño set consistente (p. ej., Chico: 4–6 px para inputs/botones; Medio: 8–12 px para cards/modales).
* [ ] **Desarrollar componentes UI núcleo (con estados coherentes: default, hover, active, focus, disabled):**

  * [ ] Botones (primario, secundario, terciario/ghost, destructivo, estilo enlace; con variantes con ícono)
  * [ ] Campos de entrada (texto, textarea, select, date picker; con etiquetas claras, placeholders, texto de ayuda, mensajes de error)
  * [ ] Checkboxes y radios
  * [ ] Toggles/switches
  * [ ] Cards (bloques de contenido, multimedia, widgets de dashboard)
  * [ ] Tablas (para datos; con headers claros; soporte de ordenado y filtrado)
  * [ ] Modales/diálogos (confirmaciones, formularios, vistas detalladas)
  * [ ] Navegación (sidebar, tabs)
  * [ ] Badges/etiquetas (estados, categorización)
  * [ ] Tooltips (ayuda contextual)
  * [ ] Indicadores de progreso (spinners, barras de progreso)
  * [ ] Íconos (usá un set único, moderno y limpio; preferentemente SVG)
  * [ ] Avatares

## III. Maquetación, jerarquía visual y estructura

* [ ] **Sistema de grilla responsivo:** diseñá sobre una grilla responsiva (p. ej., 12 columnas) para consistencia entre dispositivos.
* [ ] **Espacio en blanco estratégico:** usá espacio negativo amplio para claridad, menor carga cognitiva y balance visual.
* [ ] **Jerarquía visual clara:** guiá la mirada con tipografía (tamaño, peso, color), espaciado y posición.
* [ ] **Alineación consistente:** mantené alineaciones coherentes entre elementos.
* [ ] **Layout base del dashboard:**

  * [ ] Sidebar izquierda persistente: navegación primaria entre módulos.
  * [ ] Área de contenido: espacio principal para interfaces de cada módulo.
  * [ ] (Opcional) Barra superior: búsqueda global, perfil de usuario, notificaciones.
* [ ] **Enfoque mobile-first:** asegurá adaptación elegante a pantallas pequeñas.

## IV. Diseño de interacción y animaciones

* [ ] **Micro-interacciones con propósito:** usá animaciones sutiles y feedback visual para acciones (hover, clics, envíos de formularios, cambios de estado).

  * [ ] El feedback debe ser inmediato y claro.
  * [ ] Animaciones breves (150–300 ms) y con *easing* apropiado (p. ej., *ease-in-out*).
* [ ] **Estados de carga:** implementá indicadores claros (skeletons para páginas; spinners para acciones dentro de componentes).
* [ ] **Transiciones:** usá transiciones suaves para cambios de estado, aparición de modales y expansiones.
* [ ] **Evitá distracción:** las animaciones deben ayudar a la usabilidad, no abrumar ni ralentizar.
* [ ] **Navegación por teclado:** asegurá acceso por teclado a todos los elementos interactivos y estados de foco visibles.

## V. Tácticas específicas por módulo

### A. Módulo de moderación de multimedia

* [ ] **Visualización clara del medio:** *thumbnails* de imagen/video prominentes (vista de grilla o lista).
* [ ] **Acciones de moderación obvias:** botones claramente rotulados (Aprobar, Rechazar, Marcar, etc.) con estilo distintivo (primario/secundario, codificación por color). Usá íconos para reconocimiento rápido.
* [ ] **Indicadores de estado visibles:** badges con color para estado de contenido (Pendiente, Aprobado, Rechazado).
* [ ] **Información contextual:** metadata relevante (quién subió, timestamp, flags) junto al medio.
* [ ] **Eficiencia del flujo:**

  * [ ] Acciones masivas: selección y moderación de múltiples ítems.
  * [ ] Atajos de teclado: para acciones frecuentes.
* [ ] **Minimizar fatiga:** interfaz limpia y sin ruido; considerá opción de modo oscuro.

### B. Módulo de tablas de datos (Contactos, Configuración)

* [ ] **Legibilidad y “escaneabilidad”:**

  * [ ] Alineación inteligente: texto a la izquierda; números a la derecha.
  * [ ] Encabezados claros: headers en negrita.
  * [ ] Rayado “zebra” (opcional): útil en tablas densas.
  * [ ] Tipografía legible: sans-serif simple y limpia.
  * [ ] Altura de fila y espaciado adecuados.
* [ ] **Controles interactivos:**

  * [ ] Ordenamiento por columna: headers clickeables con indicador de orden.
  * [ ] Filtrado intuitivo: controles accesibles (dropdowns, inputs) sobre la tabla.
  * [ ] Búsqueda global en la tabla.
* [ ] **Datasets grandes:**

  * [ ] Paginación (preferida en admin) o *virtual/infinite scroll*.
  * [ ] Encabezados fijos / columnas congeladas (si aplica).
* [ ] **Interacciones por fila:**

  * [ ] Filas expandibles: para detalle.
  * [ ] Edición en línea: modificaciones rápidas.
  * [ ] Acciones masivas: checkboxes y *toolbar* contextual.
  * [ ] Íconos/botones por fila: (Editar, Eliminar, Ver) claramente distinguibles.

### C. Módulo de paneles de configuración (Microsite, Admin)

* [ ] **Claridad y simpleza:** etiquetas inequívocas; ayuda breve o tooltips. Evitá jerga.
* [ ] **Agrupación lógica:** agrupá ajustes relacionados en secciones o pestañas.
* [ ] **Revelación progresiva:** ocultá por defecto lo avanzado o poco usado (toggle “Ajustes avanzados”, acordeones).
* [ ] **Tipos de entrada adecuados:** usá controles correctos (text, checkbox, toggle, select, slider) para cada ajuste.
* [ ] **Feedback visual:** confirmación inmediata al guardar (toasts, mensajes inline). Errores claros para entradas inválidas.
* [ ] **Predeterminados sensatos:** proveé valores por defecto para todos los ajustes.
* [ ] **Opción de restablecer:** forma simple de “Restaurar valores por defecto” por sección o global.
* [ ] **Preview de micrositio (si aplica):** mostr á un preview en vivo o casi en vivo de los cambios.

## VI. Arquitectura de CSS y estilos

* [ ] **Elegir una metodología de CSS escalable:**

  * [ ] **Utility-first (recomendada para LLM):** p. ej., Tailwind CSS. Definí tokens en la config y aplicalos con utilidades.
  * [ ] **BEM con Sass:** si no usás utilidades, nomenclatura BEM con variables Sass para tokens.
  * [ ] **CSS-in-JS (estilos con *scope*):** p. ej., enfoque de Stripe para Elements.
* [ ] **Integración de design tokens:** asegurá que colores, tipografías, espaciados y radios se usen directo en la arquitectura elegida.
* [ ] **Mantenibilidad y legibilidad:** código ordenado y fácil de entender.
* [ ] **Rendimiento:** optimizá la entrega de CSS; evitá *bloat* innecesario.

## VII. Buenas prácticas generales

* [ ] **Diseño y test iterativos:** testeá continuamente con usuarios y iterá.
* [ ] **Arquitectura de información clara:** organizá contenido y navegación de forma lógica.
* [ ] **Diseño responsivo:** asegurá funcionamiento pleno y buena apariencia en desktop, tablet y mobile.
* [ ] **Documentación:** mantené documentación clara para el sistema de diseño y los componentes.
