# Create Deal with Freshworks CRM

Creates a new deal in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `api/deals`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Deal](https://developers.freshworks.com/crm/api/#create_deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal` | body | `object` | no | Deal payload object as documented by Freshworks CRM. |
| `deal.amount` | body | `number` | no | — |
| `deal.contacts_added_list[]` | body | `array<number>` | no | — |
| `deal.custom_field` | body | `object` | no | — |
| `deal.custom_field.cf_number_of_agents` | body | `number` | no | — |
| `deal.name` | body | `string` | no | — |
| `deal.sales_account` | body | `object` | no | — |
| `deal.sales_account_id` | body | `number` | no | — |
| `deal.sales_account.name` | body | `string` | no | — |
