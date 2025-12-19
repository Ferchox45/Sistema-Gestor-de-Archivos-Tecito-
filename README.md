<p align="center">
  <a href="https://www.tecnm.mx/" target="_blank">
    <img src="https://www.tecnm.mx/images/tecnm_virtual/tecnm.png" width="200" alt="Logo TecNM">
  </a>
</p>

<h1 align="center">Sistema Gestor de Archivos Académicos</h1>

<p align="center">
    Plataforma integral para la administración, carga, validación y seguimiento de evidencias académicas del Departamento de Docencia.
</p>

<p align="center">
<a href="https://laravel.com"><img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel"></a>
<a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS"></a>
<a href="https://www.mysql.com/"><img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"></a>
</p>

---

## 📖 Descripción del Proyecto

Este sistema optimiza los procesos internos del departamento de Docencia, centralizando la gestión de evidencias académicas en un entorno digital seguro. Permite estandarizar formatos, automatizar flujos de evaluación y mantener un registro histórico confiable de la actividad docente.

La plataforma está diseñada para fortalecer la comunicación entre los tres actores principales: **Docentes, Administradores y Jefes de Departamento**.

## 🚀 Funcionalidades Principales

El sistema cuenta con una arquitectura basada en roles (RBAC) que garantiza la seguridad y eficiencia operativa:

### 🛠️ Módulo de Administrador
El centro de comando para la orquestación institucional.
- **Gestión de Periodos:** Creación y parametrización de ciclos escolares (Ventana de operación) con fechas de inicio y fin.
- **Infraestructura Académica:** Gestión completa de Carreras y Materias (Altas, bajas y estatus).
- **Gestión de Usuarios:** Administración centralizada de personal con filtrado por tipo de contrato (Base, Honorario, Interino).
- **Asignación de Carga:** 
    - Asignación manual de grupos.
    - **Carga Masiva:** Importación de grupos y asignaciones mediante archivos Excel (.xlsx).

### 👨‍🏫 Módulo de Docente
Interfaz simplificada enfocada en el cumplimiento académico.
- **Dashboard Personal:** Visualización de carga académica y estatus de entregas mediante tarjetas informativas.
- **Carga de Evidencias:** Subida de archivos con validación de requisitos.
- **Sistema de Notificaciones:** Feedback en tiempo real sobre el estado de los documentos (Aprobado/Rechazado) con comentarios del revisor.
- **Gestión de Perfil:** Actualización de datos personales y seguridad.

### 📋 Módulo de Jefe de Departamento
Filtro de calidad y autoridad certificadora.
- **Flujo de Aprobación:** Revisión de documentos cargados por los docentes.
- **Firma Digital/Física:** Proceso para descargar, firmar y volver a subir documentos de alto valor (ej. Actas de Calificaciones).
- **Retroalimentación:** Capacidad de rechazar documentos con comentarios obligatorios para corrección.
- **Reportes:** Generación de reportes ejecutivos (General y Detallado) exportables a Excel para auditorías de desempeño y cumplimiento.

---

## 💻 Requisitos Previos

Asegúrate de tener instalado en tu entorno local:
* PHP >= 8.1
* Composer
* Node.js & NPM
* MySQL

---

## ⚙️ Instalación y Configuración Local

Sigue estos pasos para levantar el proyecto en tu entorno de desarrollo:

1.  **Clonar el repositorio:**
    ```bash
    git clone https://github.com/Ferchox45/Sistema-Gestor-de-Archivos-Tecito-.git
    cd Sistema-Gestor-de-Archivos-Tecito-
    ```

2.  **Instalar dependencias de Backend (Laravel):**
    ```bash
    composer install
    ```

3.  **Instalar dependencias de Frontend (NPM):**
    ```bash
    npm install
    ```

4.  **Configurar variables de entorno:**
    Copia el archivo de ejemplo y configúralo.
    ```bash
    cp .env.example .env
    ```

5.  **Configurar Base de Datos:**
    Abre el archivo `.env` y ajusta las credenciales de tu base de datos local:
    ```dotenv
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=nombre_de_tu_bd  # Asegúrate de crear esta BD en tu MySQL
    DB_USERNAME=tu_usuario
    DB_PASSWORD=tu_contraseña
    ```

6.  **Generar Key de la aplicación:**
    ```bash
    php artisan key:generate
    ```

7.  **Crear enlace simbólico para almacenamiento:**
    ```bash
    php artisan storage:link
    ```

8.  **Migración y Seeders:**
    Ejecuta las migraciones para crear las tablas e insertar los datos de prueba (usuarios, roles, etc.).
    ```bash
    php artisan migrate:refresh --seed
    ```

9.  **Compilar Assets (Tailwind CSS):**
    ```bash
    npm run dev
    ```

10. **Ejecutar el Servidor:**
    En una nueva terminal, inicia el servidor de desarrollo.
    ```bash
    php artisan serve
    ```

11. **Acceso:**
    Abre tu navegador en [http://localhost:8000](http://localhost:8000).

---

## 🔐 Credenciales de Acceso (Entorno Local)

El seeder inicial crea un usuario administrador por defecto para pruebas:

| Rol | Correo Electrónico | Contraseña |
| :--- | :--- | :--- |
| **Administrador** | `admin@correo.com` | `password` |

> **Nota:** Se recomienda cambiar esta contraseña inmediatamente después del primer inicio de sesión o crear nuevos usuarios desde el panel administrativo.

---

## 📄 Licencia

Este proyecto es software privado desarrollado para el Tecnológico Nacional de México.