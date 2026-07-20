# Update Badge with Discourse

Updates an existing badge in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/badges/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Badge](https://docs.discourse.org/#tag/Badges/operation/updateBadge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Badge id. |
| `name` | body | `string` | yes | Badge name. |
| `badge_type_id` | body | `number` | yes | Badge type id: 1 gold, 2 silver, 3 bronze. Accepted values: `0`, `1`, `2`. |
