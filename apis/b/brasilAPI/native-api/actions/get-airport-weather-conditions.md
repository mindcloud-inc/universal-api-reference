# Get Airport Weather Conditions with Brasil API

Retrieves current airport weather conditions from Brasil API by ICAO code.

## Endpoint

- **Method:** `GET`
- **Path:** `/cptec/v1/clima/aeroporto/{icaoCode}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Airport Weather Conditions](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `icaoCode` | path | `string` | yes | The 4-letter ICAO airport code. |
