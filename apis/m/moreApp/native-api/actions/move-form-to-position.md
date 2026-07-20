# Move Form To Position with MoreApp

Moves a form to a folder position in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}/move/{{position}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Move Form To Position](https://docs.moreapp.com/docs/developer-docs/01a23351e14db-move-form-to-specific-position-in-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `folderId` | path | `string` | yes |
| `formId` | path | `string` | yes |
| `position` | path | `number` | yes |
