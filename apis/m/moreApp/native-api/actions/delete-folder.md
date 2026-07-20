# Delete Folder with MoreApp

Deletes a folder from MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Delete Folder](https://docs.moreapp.com/docs/developer-docs/9a1c7d0abb95e-delete-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `folderId` | path | `string` | yes |
