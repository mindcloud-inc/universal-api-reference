# Delete Company with Upnify

Deletes an existing company from Upnify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v4/empresas/:tkEmpresa`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Delete Company](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-DeleteEmpresasTkempresa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkEmpresa` | path | `string` | yes | Código token que identifica de forma única a una empresa en el sistema, la cual será eliminada.  ¿Dónde obtengo el token? |
