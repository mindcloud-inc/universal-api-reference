# Get Message History with Salebot

## Endpoint

- **Method:** `GET`
- **Path:** `/get_history`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Get Message History](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `number` | yes | Existing Salebot client ID. |
| `limit` | query | `number` | no | Maximum history items to return, up to 2000. |
