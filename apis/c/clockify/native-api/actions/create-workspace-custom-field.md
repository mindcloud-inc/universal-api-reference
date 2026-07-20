# Create Workspace Custom Field with Clockify

Creates a workspace custom field in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/custom-fields`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Workspace Custom Field](https://docs.developer.clockify.me/#tag/Custom-fields/operation/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `name` | body | `string` | yes | — |
| `type` | body | `list<string>` | yes | Accepted values: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. |
| `allowedValues[]` | body | `array<string>` | no | — |
| `description` | body | `string` | no | — |
| `entityType` | body | `list<string>` | no | Accepted values: `TIMEENTRY`, `USER`. |
| `onlyAdminCanEdit` | body | `boolean` | no | — |
| `placeholder` | body | `string` | no | — |
| `status` | body | `list<string>` | no | Accepted values: `INACTIVE`, `INVISIBLE`, `VISIBLE`. |
| `workspaceDefaultValue` | body | `object` | no | — |
