# Update Folder Property with MoreApp

Updates a folder property in MoreApp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Folder Property](https://docs.moreapp.com/docs/developer-docs/8a56cc803116b-update-property-of-folder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json-patch+json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `folderId` | path | `string` | yes |
| `[].op` | body | `string` | yes |
| `[].path` | body | `string` | yes |
| `[].value` | body | `string` | no |
