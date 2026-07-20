# Remove User from Segment with Refiner

Removes a user from a manual segment in Refiner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sync-segment`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Remove User from Segment](https://refiner.io/docs/api/#link-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Identify the user by your own user ID. |
| `email` | query | `string` | no | Identify the user by email address. |
| `segment_uuid` | query | `string` | yes | The manual segment UUID to remove the user from. |
