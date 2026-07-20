# Generate Camp Puzzle with Shadify

Retrieves a random Camp puzzle from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/camp/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Camp Puzzle](https://shadify.yurace.pro/modules/camp.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | query | `number` | no | Optional puzzle width from 5 to 15. Default is 7. |
| `height` | query | `number` | no | Optional puzzle height from 5 to 15. Default is 7. |
| `solution` | query | `boolean` | no | Optional true or false value that includes the solution. Default is true. |
