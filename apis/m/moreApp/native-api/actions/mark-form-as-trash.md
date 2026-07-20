# Mark Form As Trash with MoreApp

Marks a form as trash in MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Mark Form As Trash](https://docs.moreapp.com/docs/developer-docs/c3ee85a1f570b-mark-form-as-trash)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
