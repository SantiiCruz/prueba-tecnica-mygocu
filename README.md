﻿# Gestión de Usuarios

Este es un proyecto creado para gestionar usuarios utilizando Vue.js y un servidor mockeado basado en un archivo OpenAPI (Swagger). El proyecto incluye las siguientes funcionalidades:

- Pantalla para listar todos los usuarios con nombre, apellido y edad calculada.
- Pantalla para agregar nuevos usuarios con validación de campos.
- **Interfaz completamente responsive**, optimizada para dispositivos móviles, tablets y pantallas de escritorio.
- Lógica del servidor mockeada automáticamente utilizando Mock Service Worker (MSW).

![Pantalla de lista de usuarios](src/assets/Listado.png)

## Características

### 1. Pantalla de Lista de Usuarios

- Muestra una lista de usuarios obtenida del servidor mock.
- Los nombres y apellidos de los usuarios se muestran concatenados en una sola línea.
- Se calcula la edad de cada usuario en función de la fecha de nacimiento proporcionada.

### 2. Pantalla de Creación de Usuarios

- Permite crear un nuevo usuario con todos los campos requeridos, siguiendo las validaciones correspondientes.
- Los campos validados incluyen nombre, apellido y fecha de nacimiento.
- El servidor mock simula la creación, aunque no persiste los nuevos usuarios en la lista.

### 3. Buenas Prácticas de Desarrollo

- El código sigue principios como Clean Code y SOLID.
- Se ha explotado la modularidad y el sistema de componentes de Vue.js para una solución escalable y fácil de mantener.

## Instalación del Proyecto

### 1. Instalación de dependencias

Para instalar las dependencias necesarias, ejecuta el siguiente comando:

```bash
npm install
```

### 2. Compilación y desarrollo

Para iniciar el servidor de desarrollo y recargar automáticamente en caliente:

```bash
npm run serve
```

### 3. Compilación para producción

Para compilar el proyecto y optimizarlo para producción:

```bash
npm run build
```

## Mock Service Worker (MSW)

Este proyecto utiliza Mock Service Worker para interceptar las solicitudes y simular un servidor basado en el archivo OpenAPI (Swagger). El servidor mock se activa automáticamente, por lo que no es necesario iniciarlo manualmente.

### Configuración de MSW

El mock de la API está configurado en src/mocks/handlers.js, donde se simulan las respuestas del servidor siguiendo las especificaciones del Swagger proporcionado.
Las respuestas incluyen una lista predefinida de usuarios para el listado, y la simulación de la creación de nuevos usuarios.

## Tecnologías Utilizadas

- Vue.js 3: Framework de desarrollo frontend progresivo.
- Vue Router: Para gestionar la navegación entre las pantallas.
- Mock Service Worker (MSW): Para mockear las respuestas del servidor de manera automática.
- ESLint: Para asegurar la calidad y consistencia del código.
