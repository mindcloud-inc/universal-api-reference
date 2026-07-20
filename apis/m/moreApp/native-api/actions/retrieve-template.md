# Retrieve Template with MoreApp

Retrieves a template from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Template](https://docs.moreapp.com/docs/developer-docs/68a89bcf059f6-get-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
