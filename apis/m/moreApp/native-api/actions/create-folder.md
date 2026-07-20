# Create Folder with MoreApp

Creates a folder in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Folder](https://docs.moreapp.com/docs/developer-docs/08e73bcc90173-create-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `meta.name` | body | `string` | yes |
