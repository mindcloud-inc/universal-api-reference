# Create Form with MoreApp

Creates a form in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/forms`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Form](https://docs.moreapp.com/docs/developer-docs/e2adf91c4478e-create-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `meta.name` | body | `string` | yes |
| `meta.description` | body | `string` | no |
