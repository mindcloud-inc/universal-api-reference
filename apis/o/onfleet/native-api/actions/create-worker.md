# Create Worker with Onfleet

Creates a new worker in Onfleet.

## Endpoint

- **Method:** `POST`
- **Path:** `/workers`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Create Worker](https://docs.onfleet.com/reference/create-worker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The worker's complete name. |
| `phone` | body | `string` | yes | The worker's phone number. |
| `teams[]` | body | `array<string>` | yes | One or more team IDs of which the worker is a member. |
| `capacity` | body | `number` | no | The maximum number of units this worker can carry. |
| `displayName` | body | `string` | no | The display name used in SMS notifications and tracking pages. |
