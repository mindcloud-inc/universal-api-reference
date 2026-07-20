# Bulk Delete Accounts with Freshworks CRM

Deletes multiple sales accounts from Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sales_accounts/bulk_destroy`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Delete Accounts](https://developers.freshworks.com/crm/api/#bulk_delete_account)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `selected_ids[]` | body | `array<number>` | yes |
