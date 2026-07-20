# List Items with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/items`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [List Items](https://www.zoho.com/books/api/v3/items/#list-items)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization. |
| `name` | query | `string` | no | Search items by name. Maximum length: 100. |
| `description` | query | `string` | no | Search items by description. Maximum length: 100. |
| `rate` | query | `number` | no | Search items by rate. |
| `tax_id` | query | `string` | no | Search items by tax ID. |
| `tax_name` | query | `string` | no | Search items by tax name. |
| `is_taxable` | query | `boolean` | no | Filter by taxable status. |
| `tax_exemption_id` | query | `string` | no | Tax exemption ID when filtering non-taxable items. |
| `account_id` | query | `string` | no | Filter by linked account ID. |
| `filter_by` | query | `list<string>` | no | Filter items by status bucket. Accepted values: `Status.Active`, `Status.All`, `Status.Inactive`. |
| `search_text` | query | `string` | no | Search items by name or description. Maximum length: 100. |
| `sat_item_key_code` | query | `string` | no | SAT item key code filter. |
| `unitkey_code` | query | `string` | no | SAT unit code filter. |
