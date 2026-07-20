# Create Prospect with Upnify

Creates a new prospect in Upnify.

## Endpoint

- **Method:** `POST`
- **Path:** `v4/prospectos`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Create Prospect](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-PostProspectos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nombre` | body | `string` | yes | Contiene el nombre del nuevo prospecto. |
| `tkEmpresa` | body | `string` | no | Código token que identifica de forma única a una empresa dentro el sistema, a la cuál pertenecerá el nuevo prospecto.  ¿Dónde obtengo el token? |
| `apellidos` | body | `string` | no | Almacena los apellidos del prospecto. |
| `titulo` | body | `string` | no | Almacena el título del prospecto. |
| `puesto` | body | `string` | no | Almacena el puesto que ocupa el prospecto en la empresa. |
| `empresa` | body | `string` | yes | Almacena el nombre de la empresa a la que pertenece el prospecto. |
| `correo` | body | `string` | no | Especifica el correo del prospecto. |
| `noEmpleado` | body | `number` | no | Especifica el número de empleado del prospecto en la empresa. |
| `calle` | body | `string` | no | Contiene el nombre o número de la calle, que forma parte de la ubicación del prospecto. |
| `colonia` | body | `string` | no | Contiene el nombre o número de la colonia, que forma parte de la ubicación del prospecto. |
| `telefono` | body | `string` | yes | Almacena el número de teléfono que pertenece al prospecto (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | body | `string` | no | En caso de existir, se guarda un número de teléfono secundario del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `movil` | body | `string` | no | Almacena un número de teléfono movil del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `idPais` | body | `string` | no | Código que indica el país del nuevo prospecto.  ¿Donde obtengo el Id? |
| `idEstado` | body | `string` | no | Código que indica un estado del país.  ¿Donde obtengo el Id? |
| `idMunicipio` | body | `string` | no | contiene un código que indica un municipio de un estado.  ¿Donde obtengo el Id? |
| `ciudad` | body | `string` | no | Contiene la ciudad del prospecto. |
| `codigoPostal` | body | `string` | no | Indica el código postal del nuevo prospecto. |
| `tkFase` | body | `string` | no | Código token que identifica de forma única a una fase dentro el sistema.  ¿Donde obtengo el Token? |
| `tkOrigen` | body | `string` | no | Código token que identifica de forma única a una fase dentro el sistema.  ¿Donde obtengo el Token? |
| `sexo` | body | `string` | no | Indica el sexo del nuevo prospecto.  - H Hombre.  - M Mujer. |
| `url` | body | `string` | no | Contiene la url del sitio web del prospecto. |
| `facebook` | body | `string` | no | Contiene la url del sitio de facebook del prospecto. |
| `twitter` | body | `string` | no | Contiene la url del sitio de twitter del prospecto. |
| `skype` | body | `string` | no | Contiene la url del sitio de skype del prospecto. |
| `linkedin` | body | `string` | no | Contiene la url del sitio de linkedin del prospecto. |
| `googlePlus` | body | `string` | no | Contiene la url del sitio de googlePlus del prospecto. |
| `comentarios` | body | `string` | no | Contiene un comentario para el nuevo prospecto. |
| `cp1` | body | `string` | no | Contiene el valor del primer campo personalizado, se pueden colocar hasta 100 y son definidos por el usuario. |
