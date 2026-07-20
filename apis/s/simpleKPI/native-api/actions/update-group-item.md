# Update Group Item with SimpleKPI

Updates an existing group item in SimpleKPI.

## Endpoint

- **Method:** `PUT`
- **Path:** `groups/:groupId/items/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Update Group Item](https://support.simplekpi.com/Developers/GroupsGroupItems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | no | The group ID. |
| `id` | path | `number` | no | The group item ID. |
| `name` | body | `string` | no | The group item name. |
| `sort_order` | body | `number` | no | The display sort order of the group item. |
