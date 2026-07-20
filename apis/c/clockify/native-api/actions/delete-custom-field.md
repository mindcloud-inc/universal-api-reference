# Delete Custom Field with Clockify

Deletes an existing custom field from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/custom-fields/:customFieldId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Custom Field](https://docs.developer.clockify.me/#tag/Custom-fields/operation/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `customFieldId` | path | `string<string>` | yes |
