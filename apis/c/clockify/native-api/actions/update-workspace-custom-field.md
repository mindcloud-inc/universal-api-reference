# Update Workspace Custom Field with Clockify

Updates a workspace custom field in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/custom-fields/:customFieldId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Workspace Custom Field](https://docs.developer.clockify.me/#tag/Custom-fields/operation/editCustomField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `customFieldId` | path | `string<string>` | yes | — |
| `name` | body | `string` | yes | Maximum length: 250. |
| `type` | body | `list<string>` | yes | Accepted values: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `allowedValues[]` | body | `array<string>` | no | — |
| `description` | body | `string` | no | — |
| `onlyAdminCanEdit` | body | `boolean` | no | — |
| `placeholder` | body | `string` | no | — |
| `required` | body | `boolean` | no | — |
| `status` | body | `list<string>` | no | Accepted values: `INACTIVE`, `INVISIBLE`, `VISIBLE`. |
| `workspaceDefaultValue` | body | `object` | no | — |
