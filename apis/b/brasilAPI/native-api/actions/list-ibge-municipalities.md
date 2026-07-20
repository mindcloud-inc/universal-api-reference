# List IBGE Municipalities with Brasil API

Retrieves IBGE municipalities from Brasil API by state abbreviation.

## Endpoint

- **Method:** `GET`
- **Path:** `/ibge/municipios/v1/{siglaUF}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [List IBGE Municipalities](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siglaUF` | path | `string` | yes | The IBGE state abbreviation. |
| `providers` | query | `string` | no | Optional comma-separated municipality data providers. |
