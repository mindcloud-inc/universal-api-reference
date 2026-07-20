# Get Sale with eGestor

Retrieves details for a sale from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendas/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Get Sale](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3733)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código da venda. |
| `listarCanceladas` | query | `boolean` | no | Define se vendas canceladas também podem ser detalhadas. |
