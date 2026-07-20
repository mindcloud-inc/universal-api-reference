# Move Form To Folder with MoreApp

Moves a form to a folder in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Move Form To Folder](https://docs.moreapp.com/docs/developer-docs/47e79e1f60727-move-form-to-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `folderId` | path | `string` | yes |
| `formId` | path | `string` | yes |
