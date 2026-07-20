# Create Deal with folk

Creates a new deal in folk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/groups/:groupId/:objectType`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Create Deal](https://developer.folk.app/api-reference/deals/create-a-deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID that owns the deal object field. |
| `objectType` | path | `string` | yes | The exact deal object type name from group custom fields, such as Deals. |
| `name` | body | `string` | yes | The display name of the deal. |
