# Update Item with Zoho Invoice

Updates an item in Zoho Invoice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:item_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Update Item](https://www.zoho.com/invoice/api/v3/items/#update-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `string` | yes | — |
| `name` | body | `string` | yes | Maximum length: 100. |
| `rate` | body | `number` | yes | — |
| `description` | body | `string` | no | Maximum length: 2000. |
| `tax_id` | body | `string` | no | — |
| `sku` | body | `string` | no | — |
| `product_type` | body | `list<string>` | no | Accepted values: `goods`, `service`. |
| `is_taxable` | body | `boolean` | no | — |
| `tax_exemption_id` | body | `string` | no | — |
| `hsn_or_sac` | body | `string` | no | — |
| `sat_item_key_code` | body | `string` | no | — |
| `unitkey_code` | body | `string` | no | — |
| `item_tax_preferences[]` | body | `array<object>` | no | — |
| `item_tax_preferences[].tax_id` | body | `string` | no | — |
| `item_tax_preferences[].tax_specification` | body | `string` | no | — |
| `custom_fields[]` | body | `array<object>` | no | — |
| `custom_fields[].customfield_id` | body | `number` | no | — |
| `custom_fields[].value` | body | `string` | no | — |
