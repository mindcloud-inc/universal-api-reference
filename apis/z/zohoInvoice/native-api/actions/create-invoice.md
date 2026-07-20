# Create Invoice with Zoho Invoice

Creates an invoice in Zoho Invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Create Invoice](https://www.zoho.com/invoice/api/v3/invoices/#create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | Unique identifier of the organization. |
| `adjustment_description` | body | `string` | no | Customize the adjustment description. |
| `avatax_exempt_no` | body | `string` | no | Avalara exemption certificate number. |
| `avatax_tax_code` | body | `string` | no | Avalara tax code. |
| `avatax_use_code` | body | `string` | no | Avalara use code. |
| `cfdi_usage` | body | `string` | no | CFDI usage code for Mexico. |
| `custom_body` | body | `string` | no | Customized email content for the invoice. |
| `custom_fields[].label` | body | `string` | no | Name of the custom field. |
| `custom_fields[].value` | body | `string` | no | Value of the custom field. |
| `custom_subject` | body | `string` | no | Customized email subject for the invoice. |
| `customer_id` | body | `string` | yes | ID of the customer to whom the invoice is created. |
| `gst_no` | body | `string` | no | GST number for the invoice. |
| `invoice_number` | body | `string` | no | Unique invoice number. |
| `invoiced_estimate_id` | body | `string` | no | ID of the estimate from which the invoice is created. |
| `line_items[].avatax_exempt_no` | body | `string` | no | Avalara exemption certificate number for the line item. |
| `line_items[].avatax_use_code` | body | `string` | no | Avalara use code for the line item. |
| `line_items[].description` | body | `string` | no | Description of the line item. |
| `line_items[].expense_id` | body | `string` | no | Expense ID associated with the line item. |
| `line_items[].hsn_or_sac` | body | `string` | no | HSN or SAC code. |
| `line_items[].name` | body | `string` | no | Name of the line item. |
| `line_items[].product_type` | body | `string` | no | Product type of the line item. |
| `line_items[].sat_item_key_code` | body | `string` | no | SAT item key code. |
| `line_items[].tax_exemption_id` | body | `string` | no | Tax exemption ID for the line item. |
| `line_items[].tax_id` | body | `string` | no | Tax ID applied to the line item. |
| `line_items[].tax_name` | body | `string` | no | Tax name for the line item. |
| `line_items[].tax_type` | body | `string` | no | Tax type for the line item. |
| `line_items[].tds_tax_id` | body | `string` | no | TDS tax ID applied to the line item. |
| `line_items[].unit` | body | `string` | no | Unit of the line item. |
| `line_items[].unitkey_code` | body | `string` | no | Unit key code. |
| `notes` | body | `string` | no | Notes added to the invoice. |
| `payment_options.payment_gateways[].additional_field1` | body | `string` | no | Provider-specific additional field for the payment gateway. |
| `payment_options.payment_gateways[].gateway_name` | body | `string` | no | Name of the payment gateway. |
| `payment_terms_label` | body | `string` | no | Override label for the payment terms. |
| `project_id` | body | `string` | no | Project ID associated with the invoice. |
| `reason` | body | `string` | no | Description of the attachment or reason field used by Zoho. |
| `recurring_invoice_id` | body | `string` | no | ID of the recurring invoice from which the invoice is created. |
| `reference_number` | body | `string` | no | Reference number for the invoice. |
| `salesperson_name` | body | `string` | no | Name of the salesperson linked to the invoice. |
| `shipping_charge` | body | `string` | no | Shipping charges applied to the invoice. |
| `tax_authority_id` | body | `string` | no | ID of the tax authority. |
| `tax_exemption_id` | body | `string` | no | ID of the tax exemption. |
| `tax_treatment` | body | `string` | no | Tax treatment for the invoice. |
| `template_id` | body | `string` | no | ID of the PDF template associated with the invoice. |
| `terms` | body | `string` | no | Terms and conditions for the invoice. |
| `date` | body | `date` | yes | Invoice date. |
| `line_items[]` | body | `array<object>` | yes | Line items of the invoice. |
| `line_items[].item_id` | body | `string` | yes | Unique item ID. |
| `line_items[].rate` | body | `number` | yes | Rate of the line item. |
| `line_items[].quantity` | body | `number` | yes | Quantity of the line item. |
| `send` | query | `boolean` | no | Send the invoice to the contact persons associated with the invoice. |
| `ignore_auto_number_generation` | query | `boolean` | no | Ignore auto invoice number generation for this invoice. |
| `contact_persons[]` | body | `array<string>` | no | IDs of the contact persons associated with the contact. |
| `payment_terms` | body | `number` | no | Payment terms in days. |
| `due_date` | body | `date` | no | Due date for the invoice. |
| `discount` | body | `number` | no | Discount applied to the invoice. |
| `discount_type` | body | `list<string>` | no | Type of discount applied to the invoice. Accepted values: `options`. |
| `is_discount_before_tax` | body | `boolean` | no | Whether discount is applied before tax. |
| `is_inclusive_tax` | body | `boolean` | no | Whether the tax is inclusive. |
| `exchange_rate` | body | `number` | no | Exchange rate of the currency. |
| `adjustment` | body | `number` | no | Adjustment made to the invoice. |
| `custom_fields[]` | body | `array<object>` | no | Custom fields for the invoice. |
| `line_items[].project_id` | body | `string` | no | Project ID associated with the line item. |
| `line_items[].time_entry_ids[]` | body | `array<string>` | no | Time entry IDs linked to the line item project. |
| `line_items[].item_order` | body | `number` | no | Display order of the line item. |
| `line_items[].discount` | body | `number` | no | Discount applied to the line item. |
| `line_items[].tax_percentage` | body | `number` | no | Tax percentage for the line item. |
| `line_items[].item_total` | body | `number` | no | Total amount of the line item. |
| `payment_options` | body | `object` | no | Payment options for the invoice. |
| `payment_options.payment_gateways[]` | body | `array<object>` | no | Payment gateways configured for the invoice. |
| `payment_options.payment_gateways[].configured` | body | `boolean` | no | Whether the payment gateway is configured. |
| `allow_partial_payments` | body | `boolean` | no | Whether partial payments are allowed for the invoice. |
| `place_of_supply` | body | `string` | no | Place of supply for GST/VAT. |
| `gst_treatment` | body | `string` | no | GST treatment for the invoice. |
| `vat_treatment` | body | `string` | no | VAT treatment for the invoice. |
