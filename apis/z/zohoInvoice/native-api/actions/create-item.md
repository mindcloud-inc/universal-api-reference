# Create Item with Zoho Invoice

Creates an item in Zoho Invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Create Item](https://www.zoho.com/invoice/api/v3/items/#create-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the item. Maximum length of the name [100] Maximum length: 100. |
| `rate` | body | `number` | yes | Per unit price of an item. |
| `description` | body | `string` | no | Description for the item. Maximum characters to be used for describing the item [2000] Maximum length: 2000. |
| `tax_id` | body | `string` | no | ID of the tax to be associated to the item. |
| `sku` | body | `string` | no | SKU or the Stock Keeping Unit value of an item, should be unique throughout the product |
| `product_type` | body | `list<string>` | no | Specify the type of an item. It can be either goods or service Accepted values: `goods`, `service`. |
| `is_taxable` | body | `boolean` | no | Boolean to track the taxability of the item. |
| `tax_exemption_id` | body | `string` | no | ID of the tax exemption applied. Mandatory, if is_taxable is false. |
| `hsn_or_sac` | body | `string` | no | HSN Code |
| `sat_item_key_code` | body | `string` | no | Add SAT Item Key Code for your goods/services. |
| `unitkey_code` | body | `string` | no | Add Unit Key Code for your goods/services. |
| `item_tax_preferences[]` | body | `array<object>` | no | ID of the tax to be associated to the item. |
| `item_tax_preferences[].tax_id` | body | `string` | no | ID of the tax to be associated to the item. |
| `item_tax_preferences[].tax_specification` | body | `string` | no | Set whether the tax type is intra/interstate |
| `custom_fields[]` | body | `array<object>` | no | Custom fields for an item. |
| `custom_fields[].customfield_id` | body | `number` | no | Unique identifier of the custom field |
| `custom_fields[].value` | body | `string` | no | Value of the Custom Field |
