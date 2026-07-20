# Generate Takuzu Puzzle with Shadify

Retrieves a random Takuzu puzzle from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/takuzu/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Takuzu Puzzle](https://shadify.yurace.pro/modules/takuzu.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `size` | query | `number` | no | Optional even field size from 4 to 12. Default is 8. |
| `fill` | query | `number` | no | Optional fill level from 0 to 100 percent. Default is 33. |
