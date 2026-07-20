# Create Product with Paycove

Creates a product in Paycove.

## Endpoint

- **Method:** `POST`
- **Path:** `products`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Create Product](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Product name. |
| `description` | body | `string` | no | Product description. |
| `crm_product_id` | body | `string` | no | External CRM product identifier. |
| `amount` | body | `number` | no | Product amount. |
| `currency` | body | `string` | no | Three-letter currency code. |
| `product_tax_code` | body | `string` | no | Product tax code. |
| `sales_tax` | body | `number` | no | Sales tax percentage. |
| `vat_tax` | body | `number` | no | VAT tax percentage. |
| `custom_fields` | body | `object` | no | Custom product fields object. |
