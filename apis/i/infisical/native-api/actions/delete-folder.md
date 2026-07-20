# Delete Folder with Infisical

Deletes an existing folder from Infisical by ID or name.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/folders/:folderIdOrName`
- **Base URL:** `https://app.infisical.com`
- **Official documentation:** [Delete Folder](https://infisical.com/docs/api-reference/endpoints/folders/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderIdOrName` | path | `string` | yes |
| `projectId` | body | `string` | yes |
| `environment` | body | `string` | yes |
