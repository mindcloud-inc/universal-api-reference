# Generate Addition Expression with Shadify

Retrieves a random addition expression from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/math/add`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Addition Expression](https://shadify.yurace.pro/modules/math.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `min-first` | query | `number` | no | Optional minimum value for the first number. Default is 1. |
| `max-first` | query | `number` | no | Optional maximum value for the first number. Default is 99. |
| `min-second` | query | `number` | no | Optional minimum value for the second number. Default is 1. |
| `max-second` | query | `number` | no | Optional maximum value for the second number. Default is 99. |
