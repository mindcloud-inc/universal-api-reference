# Update Worker with Onfleet

Updates an existing worker in Onfleet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workers/:workerId`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Update Worker](https://docs.onfleet.com/reference/update-worker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workerId` | path | `string` | yes | The Onfleet worker ID. |
| `name` | body | `string` | no | The worker's complete name. |
| `teams[]` | body | `array<string>` | no | One or more team IDs of which the worker is a member. |
