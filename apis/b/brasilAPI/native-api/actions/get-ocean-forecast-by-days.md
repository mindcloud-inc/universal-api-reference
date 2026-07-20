# Get Ocean Forecast by Days with Brasil API

Retrieves an ocean forecast from Brasil API for up to six days.

## Endpoint

- **Method:** `GET`
- **Path:** `/cptec/v1/ondas/{cityCode}/{days}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Ocean Forecast by Days](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cityCode` | path | `string` | yes | The CPTEC coastal city code. |
| `days` | path | `string` | yes | The number of ocean forecast days to return. |
