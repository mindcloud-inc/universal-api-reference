# Create Role with MoreApp

Creates a role in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers/{{customerId}}/roles`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Role](https://docs.moreapp.com/docs/developer-docs/da466a2b39bb2-create-role)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `name` | body | `string` | yes |
