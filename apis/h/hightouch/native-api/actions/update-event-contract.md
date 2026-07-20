# Update Event Contract with Hightouch

Updates an event contract in Hightouch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/events/contracts/{contractId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Update Event Contract](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The event contract ID. |
| `description` | body | `string` | no | The event contract description. |
| `name` | body | `string` | no | The event contract name. |
| `onUndeclaredSchema` | body | `string` | no | Behavior for events not defined in the contract. |
| `slug` | body | `string` | no | The event contract slug. |
| `events[]` | body | `array<object>` | no | Event definitions in the contract. |
