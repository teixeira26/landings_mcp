# 🚀 Base Community Day - Next.js + shadcn/ui + Amazon Q

Un repositorio base gratuito para el Community Day que incluye Next.js 15, shadcn/ui v4, y configuración completa de Amazon Q con MCP servers.

## 📦 ¿Qué incluye?

### Stack Tecnológico
- **Next.js 15** con Turbopack
- **React 19** 
- **TypeScript**
- **Tailwind CSS v4**
- **shadcn/ui v4** (estilo New York)
- **Lucide React** para íconos

### Configuración Amazon Q
- **MCP Servers** preconfigurados:
  - `playwright` - Automatización de navegador
  - `shadcn` - Integración con shadcn/ui
  - `context7` - Documentación de librerías
- **Rules personalizadas** para desarrollo con IA:
  - Principios de diseño de dashboards SaaS
  - Guía de desarrollo visual con Playwright

## 🚀 Inicio Rápido

### 1. Clonar el repositorio
```bash
git clone <tu-repo-url>
cd base-community-day
```

### 2. Instalar dependencias
```bash
cd my-app
npm install
```

### 3. Ejecutar en desarrollo
```bash
npm run dev
```

Abre [http://localhost:3000](http://localhost:3000) en tu navegador.

### 4. Configurar Amazon Q (Opcional)
Si usas Amazon Q, copia la configuración:
```bash
# Desde el directorio raíz del proyecto
cp -r .amazonq ~/.amazonq/
```

## 📁 Estructura del Proyecto

```
base-community-day/
├── .amazonq/                    # Configuración Amazon Q
│   ├── agents/
│   │   └── default.json        # MCP servers y herramientas
│   └── rules/
│       ├── 00-guia-visual-dev.md
│       └── 01-principios-de-diseño.md
├── my-app/                     # Aplicación Next.js
│   ├── app/
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   └── page.tsx
│   ├── components/             # Componentes shadcn/ui
│   ├── lib/
│   │   └── utils.ts
│   ├── components.json         # Configuración shadcn/ui
│   └── package.json
└── README.md
```

## 🎨 shadcn/ui Configurado

El proyecto viene con shadcn/ui v4 preconfigurado:

- **Estilo**: New York
- **Colores**: Neutral
- **CSS Variables**: Habilitadas
- **RSC**: Soporte completo
- **Íconos**: Lucide React

### Agregar componentes
```bash
npx shadcn@latest add button
npx shadcn@latest add card
npx shadcn@latest add input
```

## 🤖 Amazon Q + MCP

### MCP Servers Incluidos

#### Playwright MCP
Automatización de navegador para testing visual:
```bash
# Ejemplo de uso en Amazon Q
"Toma un screenshot de la página principal"
"Navega a /about y verifica que no hay errores en consola"
```

#### shadcn MCP  
Integración directa con shadcn/ui:
```bash
# Ejemplo de uso en Amazon Q
"Agrega un componente Button con variante destructive"
"Muestra el código del componente Card"
```

#### Context7 MCP
Documentación actualizada de librerías:
```bash
# Ejemplo de uso en Amazon Q
"Explica cómo usar React hooks"
"Muestra ejemplos de Next.js App Router"
```

### Rules Personalizadas

#### Principios de Diseño
Checklist completo para dashboards SaaS de nivel profesional inspirado en Stripe, Airbnb y Linear.

#### Guía Visual Dev
Procedimiento para validación visual automática con Playwright después de cada cambio.

## 📝 Scripts Disponibles

```bash
# Desarrollo con Turbopack
npm run dev

# Build de producción
npm run build

# Iniciar servidor de producción  
npm start

# Linting
npm run lint
```

## 🎯 Casos de Uso

Este repositorio es perfecto para:

- **Prototipos rápidos** con diseño profesional
- **Dashboards SaaS** con componentes consistentes
- **Desarrollo con IA** usando Amazon Q
- **Testing visual** automatizado
- **Workshops y demos** en Community Days

## 🛠️ Personalización

### Cambiar tema de colores
Edita `app/globals.css` para modificar las variables CSS:

```css
:root {
  --background: 0 0% 100%;
  --foreground: 240 10% 3.9%;
  /* ... más variables */
}
```

### Configurar MCP personalizado
Edita `.amazonq/agents/default.json` para agregar tus propios MCP servers.

## 📚 Recursos

- [Next.js Docs](https://nextjs.org/docs)
- [shadcn/ui Docs](https://ui.shadcn.com)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Amazon Q Developer](https://aws.amazon.com/q/developer/)

## 🤝 Contribuir

Este es un proyecto de Community Day. ¡Las contribuciones son bienvenidas!

1. Fork el proyecto
2. Crea tu feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push al branch (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 🙏 Agradecimientos

- [shadcn](https://twitter.com/shadcn) por los increíbles componentes UI
- [Vercel](https://vercel.com) por Next.js
- [AWS](https://aws.amazon.com) por Amazon Q Developer
- La comunidad de desarrolladores que hace posible estos Community Days

---

**¿Te gusta este proyecto?** ⭐ Dale una estrella en GitHub y compártelo con otros desarrolladores.
