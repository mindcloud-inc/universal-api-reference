# Create Badge with Discourse

Creates a new badge in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/badges.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Badge](https://docs.discourse.org/#tag/Badges/operation/createBadge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Badge name. |
| `badge_type_id` | body | `number` | yes | Badge type id: 1 gold, 2 silver, 3 bronze. Accepted values: `0`, `1`, `2`. |
