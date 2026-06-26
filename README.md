# Tequecoso Frontend

Frontend del proyecto **Tequecoso**, desarrollado como parte del Servicio Disciplinar CED.

Este repositorio contiene la interfaz web inicial para la gestión de clientes y proveedores, conectada al backend mediante servicios web REST construidos con Spring Boot.

## Descripción

La aplicación permite registrar clientes y proveedores desde una interfaz web simple, pensada como MVP del sistema.

Su objetivo es apoyar la digitalización básica del negocio, reemplazando parte del registro manual por formularios conectados al backend.

## Funcionalidades actuales

- Registro de clientes mediante formulario.
- Registro de proveedores mediante formulario.
- Navegación simple entre módulo de clientes y proveedores.
- Envío de datos al backend usando `fetch()` y JSON.
- Mensajes visuales de éxito o error al intentar guardar información.

## Endpoints utilizados

El frontend está preparado para conectarse a estos endpoints del backend.

### Clientes

- `GET /api/v1/client`
- `POST /api/v1/client`
- `PUT /api/v1/client/{id}`
- `DELETE /api/v1/client/{id}`

### Proveedores

- `GET /api/proveedores`
- `POST /api/proveedores`
- `PUT /api/proveedores/{id}`
- `DELETE /api/proveedores/{id}`

## Campos principales manejados

### Cliente

- `businessName`
- `rut`
- `dv`
- `contact`
- `contactName`
- `email`
- `phone`
- `phoneSecondary`
- `address`
- `city`
- `region`
- `type`
- `active`
- `notes`

### Proveedor

- `proveedor`
- `rut`
- `dv`
- `contact`
- `contactName`
- `email`
- `phone`
- `address`
- `city`
- `region`
- `category`
- `notes`

## Estructura del proyecto

```text
tequecoso-frontend/
├── index.html
└── README.md
```

En esta primera versión se trabajó en un archivo HTML único con CSS y JavaScript integrados, para acelerar el desarrollo del MVP.

## Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript
- Fetch API
- Spring Boot REST API

## Ejecución local

1. Clonar este repositorio:

```bash
git clone https://github.com/TU-USUARIO/tequecoso-frontend.git
```

2. Entrar a la carpeta del proyecto:

```bash
cd tequecoso-frontend
```

3. Abrir `index.html` en el navegador.

## Configuración de conexión

Actualmente el frontend usa la siguiente base para conectarse al backend:

```js
const API_BASE = "http://localhost:8080";
```

Si el backend corre en otro puerto o ruta base, esta constante debe modificarse en el archivo `index.html`.

## Posibles problemas

### Error de CORS

Si el frontend y el backend están corriendo en orígenes distintos, el navegador puede bloquear las peticiones.  
En ese caso, se debe habilitar CORS en la configuración del backend con Spring Boot.

### Backend apagado

Si el backend no está en ejecución, el formulario mostrará un mensaje de error al intentar registrar clientes o proveedores.

## Objetivo del módulo

Este frontend forma parte del proyecto general Tequecoso y busca apoyar la gestión administrativa básica del negocio mediante:

- registro de clientes,
- registro de proveedores,
- integración con backend,
- avance funcional para evaluación académica.

## Estado del proyecto

En desarrollo.

Versión inicial del MVP enfocada en formularios de registro e integración básica con backend.

## Autor

Repositorio frontend desarrollado para el proyecto **Tequecoso** en el contexto del Servicio Disciplinar CED.
