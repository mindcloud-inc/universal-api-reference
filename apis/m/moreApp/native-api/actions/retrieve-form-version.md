# Retrieve Form Version with MoreApp

Retrieves a form version from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Form Version](https://docs.moreapp.com/docs/developer-docs/0b97f381e2f71-get-a-specific-version-of-a-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `formVersionId` | path | `string` | yes |
