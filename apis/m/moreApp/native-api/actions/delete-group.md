# Delete Group with MoreApp

Deletes a group from MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/customers/{{customerId}}/groups/{{groupId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Delete Group](https://docs.moreapp.com/docs/developer-docs/149735c9e7cdc-delete-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `groupId` | path | `string` | yes | MoreApp group identifier. |
