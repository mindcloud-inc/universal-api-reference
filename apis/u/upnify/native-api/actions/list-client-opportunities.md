# List Client Opportunities with Upnify

Retrieves opportunities for a client in Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/clientes/:tkCliente/oportunidades`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Client Opportunities](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-GetClientesTkclienteOportunidades)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkCliente` | path | `string` | yes | El código token que identifica a un cliente de manera única dentro del CRM, del cual requerimos consultar las oportunidades asociadas.  ¿Dónde obtengo el token? |
