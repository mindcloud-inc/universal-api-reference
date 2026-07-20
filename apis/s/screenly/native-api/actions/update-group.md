# Update Group with Screenly

Updates an existing group in Screenly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:id/`
- **Base URL:** `https://api.screenlyapp.com/api/v3`
- **Official documentation:** [Update Group](https://developer.screenly.io/api/#groups_partial_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
