# Update Estimate with Zoho Invoice

Updates an estimate in Zoho Invoice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/estimates/:estimate_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Update Estimate](https://www.zoho.com/invoice/api/v3/estimates/#update-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `estimate_id` | path | `string` | yes | Unique identifier of the estimate. |
| `customer_id` | body | `string` | no | Customer ID on the estimate. |
| `line_items[]` | body | `array<object>` | no | Line items of the estimate. |
| `line_items[].item_id` | body | `string` | no | Unique ID of the item. |
| `line_items[].rate` | body | `number` | no | Rate of the line item. |
| `line_items[].quantity` | body | `number` | no | Quantity of the line item. |
| `estimate_number` | body | `string` | no | Estimate serial number. |
| `reference_number` | body | `string` | no | Transaction reference number. |
| `date` | body | `date` | no | Date on the estimate. |
| `expiry_date` | body | `date` | no | Expiration date of the estimate. |
| `ignore_auto_number_generation` | query | `boolean` | no | Ignore automatic estimate number generation and require a manual estimate number. |
