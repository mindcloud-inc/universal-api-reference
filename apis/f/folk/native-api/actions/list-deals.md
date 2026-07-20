# List Deals with folk

Retrieves a list of deals from folk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/groups/:groupId/:objectType`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [List Deals](https://developer.folk.app/api-reference/deals/list-deals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID that owns the deal object field. |
| `objectType` | path | `string` | yes | The exact deal object type name from group custom fields, such as Deals. |
