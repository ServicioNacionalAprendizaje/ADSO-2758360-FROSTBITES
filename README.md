# Documentación del Desarrollo de Software - Frostbites

## 1. Informe de Especificación de Requisitos

### Requisitos Funcionales:

- Sistema de autenticación de usuarios (registro, login y roles de usuario).
- Administración de productos (CRUD para productos y categorías).
- Carrito de compras con gestión de pedidos.
- Integración con pasarela de pagos.
- Panel de administración para gestionar ventas y usuarios.

### Requisitos No Funcionales:

- Seguridad en el acceso a la información (autenticación JWT y cifrado de contraseñas).
- Rendimiento optimizado con consultas eficientes en la base de datos.
- Implementación responsiva para compatibilidad con dispositivos móviles.
- Despliegue en Vercel (frontend), Render (backend) y Supabase (base de datos).

## 2. Documentación de Propuesta Técnica del Software

### Arquitectura:

Aplicación basada en PERN stack (PostgreSQL, Express.js, React, Node.js).

### Tecnologías utilizadas:

- **Frontend:** React.js.
- **Backend:** Node.js con Express.
- **Base de datos:** PostgreSQL.
- **Autenticación:** JSON Web Tokens (JWT).
- **Control de versiones:** Git, GitHub.

## 3. Documentación de Diseño del Software

- **Interfaces gráficas:** [Figma Design Link](https://www.figma.com/design/7GBrymPq3Tt4rJ2m82602O/FROST-BITES---WEBSITE?node-id=0-1&t=3UtewBaY5jyz2h5a-1)
- **Modelo Arquitectónico:** Basado en REST API con una estructura modular en el backend.
- **Patrones de Diseño:**
   - MVC para la organización del backend.
   - Uso de Custom Hooks en React para reutilización de lógica.
- **Modelo de Datos:** PostgreSQL con diseño relacional para productos, usuarios y pedidos. [DB Design Link](https://dbdiagram.io/d/FROST-BITES-DB-669bcca58b4bb5230ee01b93)

## 4. Artefactos de Código

### Repositorio:

[GitHub - Frostbites](https://github.com/darianmorat/frostbites/)

Contiene:

- **Frontend:** Código React.
- **Backend:** Servidor Express con controladores y rutas.

## 5. Documentación de Pruebas

### Casos de prueba:

- [Postman Link](https://www.postman.com/aerospace-architect-11303455/frostbites/overview)
- Pruebas unitarias con Jest para funciones clave.
- Pruebas de integración en endpoints de API.
- Pruebas funcionales en UI.

### Reporte de errores:

Documentado en Issues de GitHub.

## 6. Documentación de Acciones Correctivas, Preventivas y de Mejoramiento

### Historial de cambios:

Registro en commits de GitHub.

### Optimizaciones recientes:

- Mejora en consultas a la base de datos.
- Reducción del tiempo de carga de la UI.

### Seguridad:

- Implementación de validación de datos y protección contra inyecciones SQL.

## 7. Manuales

### Manual de Instalación:

Para correr el proyecto de manera local, sigue los siguientes pasos: 

#### Prerequisitos

- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [Git](https://git-scm.com/)
- [npm](https://www.npmjs.com/)

#### Paso a paso instalacion

1. Clonar el respositorio:

```bash
git clone https://github.com/darianmorat/frostbites.git
```

2. Navigar al repositorio del proyecto:

```bash
cd frostbites
```

3. Establecer variables de entorno:

```bash
# Client .env
BASE_URL=your_base_url

# Server .env
PORT=your_server_port
JWT_SECRET=your_jwt_secret_key

BASE_URL=your_base_url
DATABASE_URL=your_database_url

ADMIN_EMAIL=your_admin_email
ADMIN_ROLE=your_admin_role
USER_ROLE=your_user_role

APP_EMAIL=email_for_nodemailer
PASSWORD_APP_EMAIL=your_email_password

STRIPE_SECRET_KEY=your_secret_key
```

4. Instalar dependencias para el cliente y servidor:

```bash
# Install client dependencies
cd client && npm install

# Install server dependencies
cd ../server && npm install
```

5. Inicializar la base de datos:

```bash
# Navigate to the file directory
cd server/db

# Run the script to create tables
psql -U your_username -d your_database_name -f init.sql
```

6. Correr los entornos de desarrollo:

```bash
# For the client, start it using:
cd client && npm run dev

# For the server, start it using:
cd ../server && npm run dev
```
