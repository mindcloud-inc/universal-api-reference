# Update Badge with Absinthe

Updates an existing badge in Absinthe.

## Endpoint

- **Method:** `PUT`
- **Path:** `/badges/{badge_id}`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Update Badge](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badge_id` | path | `string` | no | UUID of the badge to update. |
| `badge_name` | body | `string` | no | Updated badge name. |
