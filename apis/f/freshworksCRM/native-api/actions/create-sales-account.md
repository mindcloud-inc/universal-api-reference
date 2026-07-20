# Create Sales Account with Freshworks CRM

Creates a new sales account in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `api/sales_accounts`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Sales Account](https://developers.freshworks.com/crm/api/#create_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sales_account` | body | `object` | no | Sales account payload object as documented by Freshworks CRM. |
| `sales_account.custom_field` | body | `object` | no | — |
| `sales_account.custom_field.cf_domain_name` | body | `string` | no | — |
| `sales_account.name` | body | `string` | no | — |
