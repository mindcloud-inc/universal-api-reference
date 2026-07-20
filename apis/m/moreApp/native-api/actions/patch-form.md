# Patch Form with MoreApp

Updates specific form properties in MoreApp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Patch Form](https://docs.moreapp.com/docs/developer-docs/fa28120e4d482-patch-specific-property-of-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `meta.description` | body | `string` | yes |
