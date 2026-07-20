# Copy Form Version To Folder with MoreApp

Copies a form version to a folder in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}/copy`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Copy Form Version To Folder](https://docs.moreapp.com/docs/developer-docs/21958495a97bc-copy-form-version-to-specified-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | — |
| `formId` | path | `string` | yes | — |
| `formVersionId` | path | `string` | yes | — |
| `brandingId` | query | `string` | no | — |
| `customerId` | body | `number` | yes | Customer ID in the request body. |
| `folderId` | body | `string` | yes | Target folder ID for the copied form version. |
| `formName` | body | `string` | yes | Name for the copied form. |
