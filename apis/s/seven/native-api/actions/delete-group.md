# Delete Group with Seven

Deletes a group from Seven.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:id`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Delete Group](https://docs.seven.io/en/rest-api/endpoints/groups#delete-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delete_contacts` | body | `boolean` | no | Specifies whether the contacts who are members of this group should also be deleted. |
| `id` | path | `number` | yes | — |
