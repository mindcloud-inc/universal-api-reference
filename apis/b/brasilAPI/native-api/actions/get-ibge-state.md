# Get IBGE State with Brasil API

Retrieves an IBGE state from Brasil API by code.

## Endpoint

- **Method:** `GET`
- **Path:** `/ibge/uf/v1/{code}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get IBGE State](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | The IBGE state code or abbreviation. |
