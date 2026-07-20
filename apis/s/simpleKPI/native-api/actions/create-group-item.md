# Create Group Item with SimpleKPI

Creates a new group item in SimpleKPI.

## Endpoint

- **Method:** `POST`
- **Path:** `groups/:groupId/items`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Create Group Item](https://support.simplekpi.com/Developers/GroupsGroupItems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | no | The group ID. |
| `name` | body | `string` | no | The group item name. |
| `sort_order` | body | `number` | no | The display sort order of the group item. |
