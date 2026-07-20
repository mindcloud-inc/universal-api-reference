# Update Prospect with Upnify

Updates an existing prospect in Upnify.

## Endpoint

- **Method:** `PUT`
- **Path:** `v4/prospectos/:tkProspecto`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Update Prospect](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-PutProspectosTkprospecto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkProspecto` | path | `string` | yes | El código token que identifica a un prospecto, al cual se requiere modificar su información.  ¿Dónde obtengo el token? |
| `aprobacionEstado` | body | `number` | no | Contiene un código que define el estado de una aprobación realizada por el usuario. |
| `esCanalizado` | body | `number` | no | Almacena un código que define si el registro se encuentra canalizado o compartido.  - 0 Registro no canalizado.  - 1 Registro original o maestro.  - 2 Registro esclavo. |
| `tkEmpresa` | body | `string` | no | Código token que identifica de forma única a una empresa dentro el sistema.  ¿Dónde obtengo el token? |
| `descartado` | body | `number` | no | Código que indica si el prospecto se encuentra descartado.  - 0 No está descartado.  - 1 Prospecto descartado. |
| `nombre` | body | `string` | no | Contiene el nombre del prospecto. |
| `apellidos` | body | `string` | no | Almacena los apellidos del prospecto. |
| `puesto` | body | `string` | no | Almacena el puesto que ocupa el prospecto en la empresa. |
| `correo` | body | `string` | no | Especifica el correo del prospecto. |
| `telefono1` | body | `string` | no | Almacena el número de teléfono que pertenece al prospecto (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | body | `string` | no | En caso de existir, se guarda un número de teléfono secundario del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `movil` | body | `string` | no | Almacena un número de teléfono movil del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `tkFase` | body | `string` | no | Codigo token que identifica de forma única a una fase dentro el sistema.  ¿Dónde obtengo el token? |
| `sexo` | body | `string` | no | Indica el sexo del nuevo prospecto. |
| `url` | body | `string` | no | Contiene la url del sitio web del prospecto. |
| `facebook` | body | `string` | no | Contiene la url del sitio de facebook del prospecto. |
| `twitter` | body | `string` | no | Contiene la url del sitio de twitter del prospecto. |
| `skype` | body | `string` | no | Contiene la url del sitio de skype del prospecto. |
| `linkedin` | body | `string` | no | Contiene la url del sitio de linkedin del prospecto. |
| `googlePlus` | body | `string` | no | Contiene la url del sitio de googlePlus del prospecto. |
| `cp1` | body | `string` | no | Contiene el valor del primer campo personalizado, se pueden colocar hasta 100 y son definidos por el usuario. |
| `tkOrigen` | body | `string` | no | Guarda el origen desde la cual se originó una oportunidad.  ¿Donde obtengo el Token? |
