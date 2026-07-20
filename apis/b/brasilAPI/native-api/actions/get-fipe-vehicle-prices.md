# Get FIPE Vehicle Prices with Brasil API

Retrieves FIPE vehicle prices from Brasil API by FIPE code.

## Endpoint

- **Method:** `GET`
- **Path:** `/fipe/preco/v1/{codigoFipe}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get FIPE Vehicle Prices](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigoFipe` | path | `string` | yes | The FIPE code to price. |
| `tabela_referencia` | query | `string` | no | Optional FIPE reference table code. |
