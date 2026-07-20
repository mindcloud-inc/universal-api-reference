# Generate Minesweeper Field with Shadify

Retrieves a random Minesweeper field from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/minesweeper/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Minesweeper Field](https://shadify.yurace.pro/modules/minesweeper.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | Required starting position as x-y. Mines are excluded around this position. |
| `width` | query | `number` | no | Optional field width. Width times height must not exceed 1000. Default is 9. |
| `height` | query | `number` | no | Optional field height. Width times height must not exceed 1000. Default is 9. |
| `mines` | query | `number` | no | Optional mine count, up to 25 percent of cells. Default is 12. |
