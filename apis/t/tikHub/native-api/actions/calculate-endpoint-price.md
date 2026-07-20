# Calculate Endpoint Price with TikHub

Calculates API endpoint pricing in TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tikhub/user/calculate_price`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Calculate Endpoint Price](https://api.tikhub.io/#/TikHub-User-API/calculate_price_api_v1_tikhub_user_calculate_price_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint` | query | `string` | yes | Requested endpoint |
| `request_per_day` | query | `number` | no | Request per day |
