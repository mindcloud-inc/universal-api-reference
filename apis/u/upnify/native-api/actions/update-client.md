# Update Client with Upnify

Updates an existing client in Upnify.

## Endpoint

- **Method:** `PUT`
- **Path:** `v4/clientes/:tkCliente`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Update Client](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-PutClientesTkcliente)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkCliente` | path | `string` | yes | El código token que identifica a un cliente de manera única dentro del CRM, al cual se requiere modificar su información.  ¿Dónde obtengo el token? |
| `aprobacionEstado` | body | `number` | yes | Código que indica si el cliente necesita ser aprobado por el dueño de la compañia con la cual se registró el prospecto.  - 0 No requiere aprobación.  - 1 Se reuiere aprobación.  </ul |
| `esCanalizado` | body | `number` | yes | Código que indica si el registro es canalizado o no. |
| `tkEmpresa` | body | `string` | yes | Código token que identifica de forma única a una empresa dentro el sistema.  ¿Dónde obtengo el token? |
| `descartado` | body | `number` | yes | Código que indica si el cliente se encuentra descartado.  - 0 Cliente no descartado.  - 1 Cliente descartado. |
| `etiquetarSeguimiento` | body | `number` | yes | Se indica si el ejecutivo puede agregar seguimientos al cliente. |
| `compartirReasignar` | body | `number` | yes | Se indica si el ejecutivo puede reasignar a un cliente. |
| `oportunidadArchivar` | body | `number` | yes | Se indica si el ejecutivo puede archivar a un cliente. |
| `descartar` | body | `number` | yes | Se indica si el ejecutivo puede descartar a un cliente. |
| `aprobar` | body | `number` | yes | Se indica si el ejecutivo puede dar la aprobación a un cliente. |
| `rechazar` | body | `number` | yes | Se indica si el ejecutivo puede rechazar un cliente. |
| `compartido` | body | `string` | yes | Indica si el cliente se encuentra actualmente compartido. |
| `emailConfigurado` | body | `string` | yes | Indica si la cuenta del ejecutivo tiene la configuración de email. |
| `esDescartado` | body | `number` | yes | Contiene un código que define si el cliente es descartado o no.  - 0 Cliente no descartado.  - 1 Cliente descartado. |
| `nombreCliente` | body | `string` | yes | Guarda el nombre del cliente. |
| `nombre` | body | `string` | yes | Contiene el nombre del cliente. |
| `apellidos` | body | `string` | yes | Almacena los apellidos del cliente. |
| `puesto` | body | `string` | yes | Almacena el puesto que ocupa el cliente en la empresa. |
| `empresa` | body | `string` | yes | Guarda el nombre de la empresa a la que pertenece el cliente. |
| `correo` | body | `string` | yes | Especifica el correo del cliente. |
| `telefono1` | body | `string` | yes | Almacena el número de teléfono que pertenece al cliente (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | body | `string` | yes | En caso de existir, se guarda un número de teléfono secundario del cliente (Si tiene un valor no númerico, devolvera un String). |
| `movil` | body | `string` | yes | Almacena un número de teléfono movil del cliente (Si tiene un valor no númerico, devolvera un String). |
| `idPais` | body | `string` | yes | Código que indica el país del nuevo prospecto.  ¿Dónde obtengo el id? |
| `idEstado` | body | `string` | yes | Código que indica un estado del país.  ¿Dónde obtengo el id? |
| `ciudad` | body | `string` | yes | Contiene la ciudad del prospecto. |
| `idMunicipio` | body | `string` | yes | contiene un código que indica un municipio de un estado.  ¿Dónde obtengo el id? |
| `tkFase` | body | `string` | yes | Código token que identifica de forma única a una fase dentro el sistema.  ¿Dónde obtengo el token? |
| `origen` | body | `string` | yes | Guarda el origen desde la cual se originó una oportunidad. |
| `proximoEvento` | body | `string` | yes | Contiene un arrelgo de datos que proporciona los datos de un evento. |
| `cp1` | body | `number` | yes | Contiene el nombre del primer campo personalizado, se pueden colocar hasta 100. |
| `pCat1` | body | `string` | yes | Primer catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para clientes, los cuales son elegidos por el usuario. |
| `eCat1` | body | `string` | yes | Primer catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para empresas, los cuales son elegidos por el usuario |
