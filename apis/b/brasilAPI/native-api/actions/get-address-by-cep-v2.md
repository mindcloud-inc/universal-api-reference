# Get Address by CEP V2 with Brasil API

Retrieves an address and geolocation from Brasil API by CEP.

## Endpoint

- **Method:** `GET`
- **Path:** `/cep/v2/{cep}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Address by CEP V2](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cep` | path | `string` | yes | The CEP to look up, with or without hyphen. |
