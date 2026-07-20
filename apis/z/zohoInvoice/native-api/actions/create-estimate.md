# Create Estimate with Zoho Invoice

Creates an estimate in Zoho Invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Create Estimate](https://www.zoho.com/invoice/api/v3/estimates/#create-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `customer_id` | body | `string` | yes | Customer ID on the estimate. |
| `line_items[]` | body | `array<object>` | yes | Line items of the estimate. |
| `line_items[].item_id` | body | `string` | yes | Unique ID of the item. |
| `line_items[].rate` | body | `number` | yes | Rate of the line item. |
| `line_items[].quantity` | body | `number` | yes | Quantity of the line item. |
| `estimate_number` | body | `string` | no | Estimate serial number. |
| `reference_number` | body | `string` | no | Transaction reference number. |
| `date` | body | `date` | no | Date on the estimate. |
| `expiry_date` | body | `date` | no | Expiration date of the estimate. |
| `notes` | body | `string` | no | Notes added below the estimate. |
| `terms` | body | `string` | no | Terms and conditions for the estimate. |
| `send` | query | `boolean` | no | Send the estimate to the associated contact persons. |
| `ignore_auto_number_generation` | query | `boolean` | no | Ignore automatic estimate number generation and require a manual estimate number. |
| `line_items[].name` | body | `string` | no | Name of the line item. |
| `line_items[].description` | body | `string` | no | Description of the line item. |
| `line_items[].unit` | body | `string` | no | Unit of measure for the line item. |
