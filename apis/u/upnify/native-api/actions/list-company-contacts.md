# List Company Contacts with Upnify

Retrieves contacts for a company in Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/empresas/:tkEmpresa/contactos`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Company Contacts](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-GetEmpresasTkempresaContactos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkEmpresa` | path | `string` | yes | Código token que identifica de forma única a una empresa en el sistema, del cual se requiere obtener los contactos asociados.  ¿Dónde obtengo el token? |
