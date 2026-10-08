# Modelo Relacional: Autenticación, Roles y Perfil 🗄️

Este documento describe el diseño del **Modelo Relacional** enfocado exclusivamente en las tres entidades fundamentales del módulo: **Roles**, **Usuarios** y **Perfil de Usuario**.

---

## 📊 Diagrama Entidad-Relación (Mermaid)

```mermaid
erDiagram
    ROLES ||--o{ USUARIOS : "asigna a"
    USUARIOS ||--|| PERFILES : "posee un"

    ROLES {
        int id_rol PK "Identificador único del rol"
        varchar nombre_rol UK "admin, cocinero, creador"
        varchar descripcion "Descripción del alcance del rol"
        boolean activo "Estado del rol"
    }

    USUARIOS {
        uuid id_usuario PK "Identificador único (UUID)"
        int id_rol FK "Referencia al rol asignado"
        varchar nombre "Nombre del usuario"
        varchar correo UK "Correo electrónico único"
        varchar contrasena "Hash de contraseña (bcrypt/Argon2)"
        timestamp ultimo_login "Fecha y hora del último acceso"
        int intentos_fallidos "Contador dinámico de intentos erróneos"
        varchar estado_cuenta "ACTIVO, BLOQUEADO, PENDIENTE"
        timestamp fecha_registro "Fecha de creación de la cuenta"
    }

    PERFILES {
        uuid id_perfil PK "Identificador único de perfil"
        uuid id_usuario FK,UK "Relación 1 a 1 única con usuarios"
        text biografia "Biografía o descripción del perfil"
        varchar avatar_url "Ruta o URL dinámica de la foto de perfil"
        varchar telefono "Número de contacto"
        timestamp actualizado_en "Última fecha de modificación del perfil"
    }
```