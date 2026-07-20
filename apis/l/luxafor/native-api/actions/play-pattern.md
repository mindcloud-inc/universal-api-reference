# Play Pattern with Luxafor

Updates a Luxafor device by playing a pattern.

## Endpoint

- **Method:** `POST`
- **Path:** `/pattern`
- **Base URL:** `https://api.luxafor.com/webhook/v1/actions`
- **Official documentation:** [Play Pattern](https://luxafor.helpscoutdocs.com/article/25-webhook-api-basics-and-guidelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionFields` | body | `object` | no | — |
| `actionFields.pattern` | body | `string` | yes | Accepted patterns: police, traffic lights, random 1, random 2, random 3, random 4, random 5. Windows-only patterns: rainbow, sea, white wave, synthetic. |
