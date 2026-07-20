# Add Custom Field with AWeber

Creates a new custom field in AWeber.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/lists/:listId/custom_fields`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Add Custom Field](https://api.aweber.com/#tag/Custom-Fields/paths/~1accounts~1{accountId}~1lists~1{listId}~1custom_fields/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `listId` | path | `string` | yes |
| `name` | body | `string` | yes |
