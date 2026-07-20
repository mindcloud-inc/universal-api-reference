# Restore Form To Active with MoreApp

Restores a form to active in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Restore Form To Active](https://docs.moreapp.com/docs/developer-docs/741525e8ed9a4-restore-form-to-active)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `formId` | path | `string` | yes |
