# Retrieve Template Version with MoreApp

Retrieves a template version from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/{{formVersionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Template Version](https://docs.moreapp.com/docs/developer-docs/8323e40d67523-get-a-specific-version-of-a-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `formVersionId` | path | `string` | yes |
| `brandingId` | query | `string` | no |
