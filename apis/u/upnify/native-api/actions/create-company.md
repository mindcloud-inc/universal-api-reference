# Create Company with Upnify

Creates a new company in Upnify.

## Endpoint

- **Method:** `POST`
- **Path:** `v4/empresas`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Create Company](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-PostEmpresas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `empresa` | body | `string` | yes | Contiene el nombre de la empresa. |
| `tkIndustria` | body | `string` | yes | Código token que identifica de forma única a una industria en el sistema.  ¿Dónde obtengo el token? |
| `url` | body | `string` | no | Contiene la dirección de la página web de la empresa. |
| `telefonoCorporativo` | body | `string` | no | Indica el número de teléfono de la nueva empresa (Si tiene un valor no númerico, devolvera un String). |
| `direccion1` | body | `string` | no | Dirección que representa la ubicación de la empresa. |
| `direccion2` | body | `string` | no | En caso de existir, se añade una segunda dirección. |
| `ciudad` | body | `string` | no | Ciudad donde se encuentra establecida la empresa. |
| `codigoPostal` | body | `string` | no | Código postal que pertenece a la zona de la empresa. |
| `idPais` | body | `string` | no | Clave del país donde se encuentra establecida la empresa.  ¿Dónde obtengo el id? |
| `idEstado` | body | `string` | no | Clave del estado del país donde se encuentra establecida la empresa.  ¿Dónde obtengo el id? |
| `idMunicipio` | body | `string` | no | Clave del municipio del estado donde se encuentra establecida la empresa.  ¿Dónde obtengo el id? |
| `numeroInterior` | body | `number` | no | Variable que forma parte de la dirección de la empresa. |
| `numeroExterior` | body | `number` | no | Variable que forma parte de la dirección de la empresa. |
| `tkCorporativo` | body | `string` | no | Código token que identifica a un Grupo de compañia. |
| `idExterno` | body | `string` | no | Identificador unico, no obligatorio para la interconexión con sistemas externos. |
| `numeroEmpleados` | body | `number` | no | Contiene un número de empleados de la empresa. |
