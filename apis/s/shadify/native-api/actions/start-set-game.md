# Start Set Game with Shadify

Retrieves a new Set game state from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/set/start`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Start Set Game](https://shadify.yurace.pro/modules/set.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `possible-sets` | query | `boolean` | no | Optional true or false value that includes possible set hints. Default is true. |
