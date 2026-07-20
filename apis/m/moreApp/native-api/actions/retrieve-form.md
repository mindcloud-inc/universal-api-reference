# Retrieve Form with MoreApp

Retrieves a form from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Form](https://docs.moreapp.com/docs/developer-docs/269963b4a5c3d-get-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
