# Generate Subtraction Expression with Shadify

Retrieves a random subtraction expression from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/math/sub`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Subtraction Expression](https://shadify.yurace.pro/modules/math.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `min-first` | query | `number` | no | Optional minimum value for the first number. Default is 1. |
| `max-first` | query | `number` | no | Optional maximum value for the first number. Default is 99. |
| `min-second` | query | `number` | no | Optional minimum value for the second number. Default is 1. |
| `max-second` | query | `number` | no | Optional maximum value for the second number. Default is 99. |
| `negative` | query | `number` | no | Optional 0 or 1 value that allows negative subtraction results. Default is 0. |
