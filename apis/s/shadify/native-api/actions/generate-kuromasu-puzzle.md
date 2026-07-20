# Generate Kuromasu Puzzle with Shadify

Retrieves a random Kuromasu puzzle from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/kuromasu/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Kuromasu Puzzle](https://shadify.yurace.pro/modules/kuromasu.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | query | `number` | no | Optional grid width from 4 to 15. Default is 5. |
| `height` | query | `number` | no | Optional grid height from 4 to 15. Default is 5. |
| `fill` | query | `number` | no | Optional ready-cell fill level from 10 to 50 percent. Default is 30. |
