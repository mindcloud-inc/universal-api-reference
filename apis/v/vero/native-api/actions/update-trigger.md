# Update Trigger with Vero

Updates an existing trigger in Vero.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/triggers/:id`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Update Trigger](https://help.getvero.com/api-reference/trigger/updates-a-trigger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The trigger identifier. |
| `type` | body | `string` | no | Optional trigger type update. |
| `event` | body | `object` | no | Optional trigger event object update. |
| `schedule` | body | `object` | no | Optional trigger schedule object update. |
| `recurring` | body | `boolean` | no | Optional recurring flag update. |
| `immediate` | body | `boolean` | no | Optional immediate flag update. |
