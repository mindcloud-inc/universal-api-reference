# List Financial Event Installments with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/financeiro/eventos-financeiros/{id_evento}/parcelas`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [List Financial Event Installments](https://developers.contaazul.com/open-api-docs/financial-apis-openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_evento` | path | `string` | yes | Conta Azul financial event identifier from the path. |
