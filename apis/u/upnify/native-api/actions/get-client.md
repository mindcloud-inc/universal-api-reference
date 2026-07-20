# Get Client with Upnify

Retrieves a client from Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/clientes/:tkCliente`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Get Client](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-GetClientesTkcliente)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkCliente` | path | `string` | yes | El código token que identifica a un cliente de manera única dentro del CRM, del cual se requiere obtener los detalles.  ¿Dónde obtengo el token? |
