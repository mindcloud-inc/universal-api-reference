# List Template Versions with MoreApp

Retrieves template versions from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Template Versions](https://docs.moreapp.com/docs/developer-docs/a10fa9e66b164-get-versions-of-a-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
| `page` | query | `number` | no |
| `size` | query | `number` | no |
| `brandingId` | query | `string` | no |
