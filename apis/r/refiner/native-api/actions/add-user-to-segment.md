# Add User to Segment with Refiner

Adds a user to a manual segment in Refiner.

## Endpoint

- **Method:** `POST`
- **Path:** `/sync-segment`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Add User to Segment](https://refiner.io/docs/api/#link-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Identify the user by your own user ID. |
| `email` | body | `string` | no | Identify the user by email address. |
| `segment_uuid` | body | `string` | yes | The manual segment UUID to add the user to. |
