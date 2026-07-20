# Delete Form Version with MoreApp

Deletes a form version from MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Delete Form Version](https://docs.moreapp.com/docs/developer-docs/8bb61d4e4461b-delete-form-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `formVersionId` | path | `string` | yes |
