# Restore Template To Active with MoreApp

Restores a template to active in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Restore Template To Active](https://docs.moreapp.com/docs/developer-docs/8e45a4386d0e8-restore-template-to-active)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
