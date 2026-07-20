# Mark Template As Trash with MoreApp

Marks a template as trash in MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Mark Template As Trash](https://docs.moreapp.com/docs/developer-docs/ab3f447dabd14-mark-template-as-trash)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
