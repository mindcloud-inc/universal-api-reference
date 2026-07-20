# Get Address by CEP with Brasil API

Retrieves an address from Brasil API by CEP.

## Endpoint

- **Method:** `GET`
- **Path:** `/cep/v1/{cep}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Address by CEP](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cep` | path | `string` | yes | The 8-digit CEP to look up. |
