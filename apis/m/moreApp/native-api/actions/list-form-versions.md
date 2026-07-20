# List Form Versions with MoreApp

Retrieves form versions from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Form Versions](https://docs.moreapp.com/docs/developer-docs/d731a224934e1-get-versions-of-a-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
