# Get Ocean Forecast with Brasil API

Retrieves a one-day ocean forecast from Brasil API.

## Endpoint

- **Method:** `GET`
- **Path:** `/cptec/v1/ondas/{cityCode}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Ocean Forecast](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cityCode` | path | `string` | yes | The CPTEC coastal city code. |
