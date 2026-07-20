# List FIPE Brands with Brasil API

Retrieves FIPE brands from Brasil API by vehicle type.

## Endpoint

- **Method:** `GET`
- **Path:** `/fipe/marcas/v1/{tipoVeiculo}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [List FIPE Brands](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tipoVeiculo` | path | `string` | yes | The FIPE vehicle type. |
| `tabela_referencia` | query | `string` | no | Optional FIPE reference table code. |
