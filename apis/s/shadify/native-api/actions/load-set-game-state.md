# Load Set Game State with Shadify

Retrieves a Set game state from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/set/:state`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Load Set Game State](https://shadify.yurace.pro/modules/set.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | path | `string` | yes | Required Set game state string from a previous Start Set Game response. |
| `possible-sets` | query | `boolean` | no | Optional true or false value that includes possible set hints. Default is true. |
| `action` | query | `string` | no | Optional add or remove action for the current Set game state. |
| `cards` | query | `string` | no | Required for action=remove. Dash-joined card IDs such as 1-2-3. |
