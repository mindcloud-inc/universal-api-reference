# Delete Group Item with SimpleKPI

Deletes an existing group item from SimpleKPI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/:groupId/items/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Delete Group Item](https://support.simplekpi.com/Developers/GroupsGroupItems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | no | The group ID. |
| `id` | path | `number` | no | The group item ID. |
