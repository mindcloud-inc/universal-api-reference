# Finalize Form Version with MoreApp

Finalizes a form version for publishing in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}/finalize`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Finalize Form Version](https://docs.moreapp.com/docs/developer-docs/7a8379cd18397-finalize-for-publish-form-version)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `formVersionId` | path | `string` | yes |
| `brandingId` | query | `string` | no |
