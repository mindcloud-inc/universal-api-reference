# Create Client with Upnify

Creates a new client in Upnify.

## Endpoint

- **Method:** `POST`
- **Path:** `v4/clientes`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Create Client](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-PostClientes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nombre` | body | `string` | yes | Contiene el nombre del nuevo cliente. |
| `tkEmpresa` | body | `string` | no | Código token que identifica de forma única a una empresa dentro el sistema, a la cuál pertenecerá el nuevo cliente.  ¿Dónde obtengo el token? |
| `apellidos` | body | `string` | no | Almacena los apellidos del cliente. |
| `titulo` | body | `string` | no | Almacena el título del cliente. |
| `puesto` | body | `string` | no | Almacena el puesto que ocupa el cliente en la empresa. |
| `empresa` | body | `string` | yes | Almacena el nombre de la empresa a la que pertenece el cliente. |
| `correo` | body | `string` | no | Especifica el correo del cliente. |
| `noEmpleado` | body | `number` | no | Especifica el número de empleado del cliente en la empresa. |
| `calle` | body | `string` | no | Contiene el nombre o número de la calle, que forma parte de la ubicación del cliente. |
| `colonia` | body | `string` | no | Contiene el nombre o número de la colonia, que forma parte de la ubicación del cliente. |
| `telefono` | body | `string` | yes | Almacena el número de teléfono que pertenece al cliente (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | body | `string` | no | En caso de existir, se guarda un número de teléfono secundario del cliente (Si tiene un valor no númerico, devolvera un String). |
| `movil` | body | `string` | no | Almacena un número de teléfono movil del cliente (Si tiene un valor no númerico, devolvera un String). |
| `idPais` | body | `string` | no | Código que indica el país del nuevo cliente.  ¿Donde obtengo el Id? |
| `idEstado` | body | `string` | no | Código que indica un estado del país.  ¿Donde obtengo el Id? |
| `idMunicipio` | body | `string` | no | contiene un código que indica un municipio de un estado.  ¿Donde obtengo el Id? |
| `ciudad` | body | `string` | no | Contiene la ciudad del cliente. |
| `codigoPostal` | body | `string` | no | Indica el código postal del nuevo cliente. |
| `tkFase` | body | `string` | no | Código token que identifica de forma única a una fase dentro el sistema.  ¿Donde obtengo el Token? |
| `tkOrigen` | body | `string` | no | Código token que identifica de forma única a una fase dentro el sistema.  ¿Donde obtengo el Token? |
| `sexo` | body | `string` | no | Indica el sexo del nuevo cliente.  - H Hombre.  - M Mujer. |
| `url` | body | `string` | no | Contiene la url del sitio web del cliente. |
| `facebook` | body | `string` | no | Contiene la url del sitio de facebook del cliente. |
| `twitter` | body | `string` | no | Contiene la url del sitio de twitter del cliente. |
| `skype` | body | `string` | no | Contiene la url del sitio de skype del cliente. |
| `linkedin` | body | `string` | no | Contiene la url del sitio de linkedin del cliente. |
| `googlePlus` | body | `string` | no | Contiene la url del sitio de googlePlus del cliente. |
| `comentarios` | body | `string` | no | Contiene un comentario para el nuevo cliente. |
| `cp1` | body | `string` | no | Contiene el valor del primer campo personalizado, se pueden colocar hasta 100 y son definidos por el usuario. |
