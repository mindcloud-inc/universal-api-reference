# Register Content Action with Giphy

Registers a GIF or sticker interaction in Giphy analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `https://giphy-analytics.giphy.com/v2/pingback_simple`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Register Content Action](https://developers.giphy.com/docs/api/endpoint/#action-register)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `analytics_response_payload` | query | `string` | yes |
| `action_type` | query | `string` | yes |
| `random_id` | query | `string` | yes |
| `ts` | query | `number` | yes |
