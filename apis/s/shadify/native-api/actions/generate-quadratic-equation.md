# Generate Quadratic Equation with Shadify

Retrieves a random quadratic equation from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/math/quad`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Quadratic Equation](https://shadify.yurace.pro/modules/math.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `min-a` | query | `number` | no | Optional minimum value for coefficient A. Default is 1. |
| `max-a` | query | `number` | no | Optional maximum value for coefficient A. Default is 20. |
| `min-b` | query | `number` | no | Optional minimum value for coefficient B. Default is 1. |
| `max-b` | query | `number` | no | Optional maximum value for coefficient B. Default is 40. |
| `min-c` | query | `number` | no | Optional minimum value for coefficient C. Default is 1. |
| `max-c` | query | `number` | no | Optional maximum value for coefficient C. Default is 20. |
