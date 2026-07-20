# Create Template with MoreApp

Creates a template in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/forms/customer/{{customerId}}/templates`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Template](https://docs.moreapp.com/docs/developer-docs/14b8ea3c3ed4f-create-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `meta.name` | body | `string` | yes |
| `meta.description` | body | `string` | no |
