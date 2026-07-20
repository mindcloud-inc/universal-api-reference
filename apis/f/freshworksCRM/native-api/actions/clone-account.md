# Clone Account with Freshworks CRM

Creates a sales account by cloning one in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sales_accounts/:id/clone`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Clone Account](https://developers.freshworks.com/crm/api/#clone_an_account)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `sales_account` | body | `object` | yes |
| `sales_account.name` | body | `string` | yes |
