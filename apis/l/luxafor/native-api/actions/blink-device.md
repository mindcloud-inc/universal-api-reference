# Blink Device with Luxafor

Updates a Luxafor device by blinking it.

## Endpoint

- **Method:** `POST`
- **Path:** `/blink`
- **Base URL:** `https://api.luxafor.com/webhook/v1/actions`
- **Official documentation:** [Blink Device](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionFields` | body | `object` | no | — |
| `actionFields.color` | body | `string` | yes | Accepted colors: red, green, yellow, blue, white, cyan, magenta. |
