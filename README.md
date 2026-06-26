# Tequecoso Frontend

Frontend del proyecto **Tequecoso**, desarrollado como parte del Servicio Disciplinar CED.  
Este repositorio contiene la interfaz web inicial para la gestión de clientes y proveedores, conectada mediante `fetch()` a los servicios web REST desarrollados en Spring Boot [file:24][file:7].

## Descripción

La aplicación permite registrar clientes y proveedores desde una interfaz web simple, pensada como MVP del sistema.  
Su objetivo es apoyar la digitalización básica del negocio, reemplazando parte del registro manual por formularios conectados al backend [file:7][file:24].

## Funcionalidades actuales

- Registro de clientes mediante formulario.
- Registro de proveedores mediante formulario.
- Navegación simple entre módulo de clientes y proveedores.
- Envío de datos al backend usando `fetch()` y JSON.
- Mensajes visuales de éxito o error al intentar guardar información [query].

## Endpoints utilizados

El frontend está preparado para conectarse a estos endpoints del backend:

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

Estas rutas fueron definidas a partir de los controladores del backend compartidos durante el desarrollo [query].

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

Los nombres de los campos se alinearon con los modelos Java del backend para facilitar el mapeo automático de JSON con Spring Boot [query].

## Estructura del proyecto

```text
tequecoso-frontend/
├── index.html
└── README.md
```

En esta primera versión se trabajó en un archivo HTML único con CSS y JavaScript integrados, para acelerar el desarrollo del MVP y facilitar la evidencia de avance para la evaluación [file:7].

## Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript
- Fetch API
- Spring Boot REST API (backend relacionado) [file:24]

## Ejecución local

1. Clonar este repositorio:
```bash
git clone https://github.com/TU-USUARIO/tequecoso-frontend.git
```

2. Entrar a la carpeta:
```bash
cd tequecoso-frontend
```

3. Abrir `index.html` en el navegador.

## Requisito importante

Para que el registro funcione correctamente, el backend debe estar levantado localmente.  
Actualmente el frontend usa como base:

```js
const API_BASE = "http://localhost:8080";
```

Si el backend corre en otro puerto o ruta base, esa constante debe ajustarse [query].

## Posibles problemas

### Error de CORS
Si el frontend está abierto desde un origen distinto al backend, el navegador puede bloquear las peticiones por política CORS.  
Ese comportamiento es común cuando frontend y backend corren en distintos puertos, y en Spring Boot se resuelve habilitando CORS en el controlador o en la configuración global [web:455][web:486].

### Backend apagado
Si Spring Boot no está corriendo, el formulario mostrará mensajes de error al intentar registrar clientes o proveedores [query].

## Objetivo académico

Este frontend forma parte del proyecto de curso orientado a:
- gestionar clientes y proveedores,
- apoyar el control administrativo básico,
- integrarse con servicios web,
- y aportar evidencia funcional para la evaluación del ramo [file:7][file:24].

## Estado del proyecto

En desarrollo.  
Versión inicial del MVP enfocada en formularios de registro e integración básica con backend [file:7].

## Relación con el proyecto principal

Este repositorio corresponde al módulo frontend del proyecto general Tequecoso.  
El repositorio principal del curso centraliza documentación, BPMN, evidencias, actas y enlaces a los distintos componentes del sistema [file:24].
