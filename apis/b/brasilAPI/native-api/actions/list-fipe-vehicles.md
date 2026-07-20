# List FIPE Vehicles with Brasil API

Retrieves FIPE vehicles from Brasil API by brand and vehicle type.

## Endpoint

- **Method:** `GET`
- **Path:** `/fipe/veiculos/v1/{tipoVeiculo}/{codigoMarca}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [List FIPE Vehicles](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tipoVeiculo` | path | `string` | yes | The FIPE vehicle type. |
| `codigoMarca` | path | `string` | yes | The FIPE brand code. |
| `tabela_referencia` | query | `string` | no | Optional FIPE reference table code. |
