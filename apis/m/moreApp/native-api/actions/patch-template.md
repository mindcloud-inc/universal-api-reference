# Patch Template with MoreApp

Updates specific template properties in MoreApp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Patch Template](https://docs.moreapp.com/docs/developer-docs/049ea5e5cf21c-patch-specific-property-of-a-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `meta.description` | body | `string` | yes |
