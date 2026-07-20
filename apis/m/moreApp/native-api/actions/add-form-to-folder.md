# Add Form To Folder with MoreApp

Adds a form to a folder in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Add Form To Folder](https://docs.moreapp.com/docs/developer-docs/d057b1cf39424-add-form-to-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `folderId` | path | `string` | yes |
| `formId` | path | `string` | yes |
