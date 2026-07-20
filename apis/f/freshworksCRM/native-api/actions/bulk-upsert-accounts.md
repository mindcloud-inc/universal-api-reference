# Bulk Upsert Accounts with Freshworks CRM

Finds or creates multiple sales accounts in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sales_accounts/bulk_upsert`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Upsert Accounts](https://developers.freshworks.com/crm/api/#bulk_upsert_account)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sales_accounts[]` | body | `array<object>` | yes |
| `sales_accounts[].data` | body | `object` | no |
| `sales_accounts[].data.city` | body | `string` | no |
| `sales_accounts[].id` | body | `string` | no |
| `sales_accounts[].name` | body | `string` | no |
