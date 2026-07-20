# Get City Weather Forecast by Days with Brasil API

Retrieves a city weather forecast from Brasil API for up to six days.

## Endpoint

- **Method:** `GET`
- **Path:** `/cptec/v1/clima/previsao/{cityCode}/{days}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get City Weather Forecast by Days](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cityCode` | path | `string` | yes | The CPTEC city code. |
| `days` | path | `string` | yes | The number of forecast days to return. |
