# Get Form Template with MoreApp

Retrieves a form template from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/templates/{{formVersionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Get Form Template](https://docs.moreapp.com/docs/developer-docs/6f629f56cb4be-get-a-form-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formVersionId` | path | `string` | yes |
| `brandingId` | query | `string` | no |
