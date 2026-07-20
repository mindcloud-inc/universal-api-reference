# Upsert Account with Freshworks CRM

Finds a sales account in Freshworks CRM, or creates one when none match.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sales_accounts/upsert`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Upsert Account](https://developers.freshworks.com/crm/api/#upsert_an_account)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sales_account` | body | `object` | yes |
| `sales_account.city` | body | `string` | no |
| `unique_identifier` | body | `object` | yes |
| `unique_identifier.name` | body | `string` | yes |
