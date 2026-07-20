# Retrieve Folder with MoreApp

Retrieves a folder from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Folder](https://docs.moreapp.com/docs/developer-docs/2bce680f6a839-get-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `folderId` | path | `string` | yes |
