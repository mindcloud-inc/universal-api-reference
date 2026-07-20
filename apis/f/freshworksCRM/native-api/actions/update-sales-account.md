# Update Sales Account with Freshworks CRM

Updates an existing sales account in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/sales_accounts/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Sales Account](https://developers.freshworks.com/crm/api/#update_a_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | Unique sales account identifier. |
| `sales_account.custom_field` | body | `object` | no | — |
| `sales_account.custom_field.cf_domain_name` | body | `string` | no | — |
| `sales_account` | body | `object` | no | Sales account fields to update. |
