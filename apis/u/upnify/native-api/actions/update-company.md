# Update Company with Upnify

Updates an existing company in Upnify.

## Endpoint

- **Method:** `PUT`
- **Path:** `v4/empresas/:tkEmpresa`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Update Company](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-PutEmpresasTkempresa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkEmpresa` | path | `string` | yes | Código token que identifica de forma única a una empresa en el sistema, la cual se requiere modificar.  ¿Dónde obtengo el token? |
| `empresa` | body | `string` | yes | Contiene el nombre de la empresa. |
| `url` | body | `string` | yes | Contiene la dirección de la página web de la empresa. |
| `telefonoCorporativo` | body | `string` | yes | Indica el número de teléfono de la nueva empresa (Si tiene un valor no númerico, devolvera un String). |
| `tkIndustria` | body | `string` | yes | Código token que identifica de forma única a una industria en el sistema.  ¿Dónde obtengo el token? |
| `direccion1` | body | `string` | yes | Dirección que representa la ubicación de la empresa. |
| `direccion2` | body | `string` | yes | En caso de existir, se añade una segunda dirección. |
| `ciudad` | body | `string` | yes | Ciudad donde se encuentra establecida la empresa. |
| `codigoPostal` | body | `string` | yes | Código postal que pertenece a la zona de la empresa. |
| `idPais` | body | `string` | yes | Clave del país donde se encuentra establecida la empresa.  ¿Dónde obtengo el id? |
| `idEstado` | body | `string` | yes | Clave del estado del país donde se encuentra establecida la empresa.  ¿Dónde obtengo el id? |
| `idMunicipio` | body | `string` | yes | Clave del municipio del estado donde se encuentra establecida la empresa.  ¿Dónde obtengo el id? |
| `numeroInterior` | body | `number` | yes | Variable que forma parte de la dirección de la empresa. |
| `numeroExterior` | body | `number` | yes | Variable que forma parte de la dirección de la empresa. |
| `tkCorporativo` | body | `string` | yes | Código token que identifica a un Grupo de compañia. |
| `idExterno` | body | `string` | yes | Identificador unico, no obligatorio para la interconexión con sistemas externos. |
| `numeroEmpleados` | body | `number` | yes | Contiene un número de empleados de la empresa. |
