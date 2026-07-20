# Remove Form From Folder with MoreApp

Removes a form from a folder in MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Remove Form From Folder](https://docs.moreapp.com/docs/developer-docs/982e234d5b352-remove-form-from-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `folderId` | path | `string` | yes |
| `formId` | path | `string` | yes |
