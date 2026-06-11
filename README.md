# Práctica 09: Validaciones Avanzadas

Práctica enfocada en la implementación de un sistema de validación robusto en dos capas (Frontend y Backend), garantizando una experiencia de usuario fluida y la integridad total de los datos.

## Descripción del Proyecto
El objetivo principal es asegurar que los datos enviados al servidor sean siempre válidos. Se implementaron Laravel Form Requests en el backend para la seguridad del servidor y VeeValidate + Yup en el frontend para la validación en tiempo real. Esta arquitectura asegura que los errores sean comunicados al usuario de forma clara, específica y multilingüe (español).

## Tecnologías Utilizadas

### Backend
- **Laravel Form Requests:** Centralización de las reglas de validación en clases dedicadas (StoreProductoRequest) .  
- **Mensajes Personalizados:** Configuración de retroalimentación en español mediante el método messages() para mejorar la usabilidad .  
- **Arquitectura REST:** Respuesta automática de errores con código HTTP 422 (Unprocessable Entity) . 

### Frontend
- **VeeValidate & Yup:** Esquemas de validación reactivos (productoSchema) que espejan las reglas del servidor .  
- **Componentes Reutilizables:** Creación de InputField.vue para estandarizar la entrada de datos y el manejo de errores .  
- **Sincronización de Errores:** Manejo de promesas (async/await) para capturar y mapear errores del servidor hacia la interfaz de usuario .

## Características Implementadas
- **Validación Dual:** Protección redundante que mejora la UX (frontend) y garantiza la seguridad (backend).  
- **Errores Campo por Campo:** Mensajes de error específicos que aparecen exactamente debajo del input afectado .  
- **Validación en Tiempo Real:** Feedback inmediato mientras el usuario escribe mediante esquemas de Yup.  
- **Componente InputField:** Abstracción de la lógica de inputs para evitar repetición de código en las vistas de creación y edición . 

## Instrucciones de Instalación

### Backend (Laravel)
```bash
# Crear los Form Requests
php artisan make:request StoreProductoRequest
php artisan make:request UpdateProductoRequest
# Asegurarse de usar los Requests en el Controlador
```

## Frontend (Vue.js)
```bash
npm install vee-validate yup
# Crear el schema en src/schemas/productoSchema.js
# Registrar el componente InputField.vue en tus vistas
```

**Desarrollado por:** Jared Hernández González - Universidad Politécnica de Texcoco (UPTex) 