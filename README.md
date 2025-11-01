# 🚀 Ideas Browser - Plataforma de Descubrimiento de Tendencias

**Versión**: 1.0.0  
**Estado**: En Desarrollo Activo  
**Última Actualización**: Noviembre 2025

## 📋 Descripción

Ideas Browser es una plataforma SaaS innovadora diseñada para emprendedores y gestores de productos que desean identificar tendencias emergentes, nichos sin explorar y oportunidades de negocio prometedoras.

La aplicación recopila y analiza datos de múltiples fuentes (Reddit, YouTube, Twitter/X) utilizando inteligencia artificial para detectar patrones, tendencias y oportunidades que otros podrían pasar por alto.

## ✨ Características Principales

- **🔍 Análisis de Tendencias**: Detecta automáticamente ideas emergentes y oportunidades de negocio
- **🌐 Integración Multi-Fuente**: Recopila datos de Reddit, YouTube, Twitter/X y más
- **🤖 Análisis con IA**: Utiliza procesamiento avanzado para insights relevantes
- **💾 Gestión de Ideas**: Guarda, organiza y etiqueta ideas para seguimiento
- **📊 Visualización de Datos**: Gráficas y análisis de tendencias en tiempo real
- **🔐 Autenticación Segura**: Sistema JWT con tokens refresh automáticos
- **🎨 Interfaz Profesional**: Diseño moderno y responsive para todos los dispositivos

## 🛠️ Tech Stack

### Frontend
- **Next.js 15** - Framework React con SSR
- **TypeScript** - Tipado estricto
- **Tailwind CSS** - Estilos modernos
- **shadcn/ui** - Componentes reutilizables
- **React Query** - Manejo de estado

### Backend
- **Express.js** - Framework HTTP
- **Node.js** - Runtime JavaScript
- **MongoDB** - Base de datos NoSQL
- **Mongoose** - ODM para MongoDB
- **JWT** - Autenticación

### DevOps
- **Docker** - Containerización
- **Docker Compose** - Orquestación local
- **TypeScript** - Tipado en todo el stack

## 📁 Estructura del Proyecto

```
IdeasApps/
├── frontend/                 # Aplicación Next.js
├── backend/                  # API Express.js
├── database/                 # Configuración de BD
├── docs/                     # Documentación
├── .cursorrules              # Reglas para Cursor AI
├── docker-compose.yml        # Composición Docker
├── package.json              # Dependencias raíz
└── README.md                 # Este archivo
```

## 🚀 Inicio Rápido

### Requisitos Previos
- Node.js 18+
- npm o yarn
- Docker y Docker Compose (opcional)
- MongoDB local o Atlas

### Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/IdeasApps.git
   cd IdeasApps
   ```

2. **Instalar dependencias**
   ```bash
   npm install
   ```

3. **Configurar variables de entorno**
   ```bash
   cp .env.example .env.local
   ```

4. **Ejecutar en desarrollo**
   ```bash
   npm run dev
   ```

### Con Docker

```bash
docker-compose up -d
```

## 📖 Documentación

- [INSTRUCCIONES_APP.md](./INSTRUCCIONES_APP.md) - Especificaciones detalladas
- [.cursorrules](./.cursorrules) - Guías de desarrollo
- [CURSOR_PROMPT.md](./CURSOR_PROMPT.md) - Prompt para Cursor AI

## 🔐 Variables de Entorno

Copia `.env.example` a `.env.local` y configura:

```env
# Database
MONGODB_URI=mongodb+srv://user:pass@cluster.mongodb.net/ideas-browser

# JWT
JWT_SECRET=tu_secreto_muy_seguro_aqui
JWT_EXPIRE=7d

# APIs
REDDIT_API_KEY=tu_reddit_key
YOUTUBE_API_KEY=tu_youtube_key

# Server
PORT=5000
NODE_ENV=development
```

## 📝 Endpoints Principales (API v1)

### Autenticación
- `POST /api/v1/auth/register` - Registro de usuario
- `POST /api/v1/auth/login` - Login
- `POST /api/v1/auth/refresh` - Refresh token

### Ideas
- `GET /api/v1/ideas` - Listar ideas
- `POST /api/v1/ideas` - Crear idea
- `GET /api/v1/ideas/:id` - Obtener idea
- `PUT /api/v1/ideas/:id` - Actualizar idea
- `DELETE /api/v1/ideas/:id` - Eliminar idea

### Integraciones
- `GET /api/v1/integrations/reddit/status` - Estado de Reddit
- `GET /api/v1/integrations/youtube/status` - Estado de YouTube

## 🧪 Testing

```bash
# Tests unitarios
npm run test

# Tests de integración
npm run test:integration

# Cobertura
npm run test:coverage
```

## 📊 Estándares de Código

```bash
# Lint
npm run lint

# Formato
npm run format
```

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](./LICENSE) para detalles.

## 👨‍💻 Autor

**Ideas Browser Team**

## 🙏 Agradecimientos

- Gracias a la comunidad de desarrolladores
- Inspiración en Greg Isenberg y metodologías de descubrimiento de ideas

---

**¿Preguntas?** Abre un issue o contacta al equipo.  
**¿Quieres contribuir?** Consulta nuestra documentación de desarrollo.
