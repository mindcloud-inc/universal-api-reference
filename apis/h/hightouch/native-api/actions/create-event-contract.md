# Create Event Contract with Hightouch

Creates a new event contract in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/contracts`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Create Event Contract](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The event contract description. |
| `name` | body | `string` | yes | The event contract name. |
| `onUndeclaredSchema` | body | `string` | no | Behavior for events not defined in the contract. |
| `slug` | body | `string` | no | The event contract slug. If omitted, Hightouch generates one. |
| `events[]` | body | `array<object>` | no | Event definitions in the contract. |
