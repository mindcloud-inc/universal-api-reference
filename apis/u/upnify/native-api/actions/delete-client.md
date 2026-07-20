# Delete Client with Upnify

Deletes an existing client from Upnify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v4/clientes/:tkCliente`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Delete Client](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-DeleteClientesTkcliente)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkCliente` | path | `string` | yes | El código token que identifica a un cliente de manera única dentro del CRM, el cual se requiere descartar.  ¿Dónde obtengo el token? |
| `tkRazonPerdida` | query | `string` | yes | Código token que corresponde a una razón de descartado.  ¿Dónde obtengo el token? |
