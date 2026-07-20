# Create Invoice with Finmei

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://app.finmei.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buyer` | body | `object` | yes | Buyer object. |
| `buyer.country` | body | `string` | yes | Buyer country code. |
| `buyer.first_name` | body | `string` | yes | Buyer first name. |
| `buyer.last_name` | body | `string` | yes | Buyer last name. |
| `buyer.type` | body | `string` | yes | Buyer type. |
| `currency` | body | `string` | yes | Invoice currency code. |
| `invoice_date` | body | `string` | yes | Invoice issue date. |
| `products` | body | `list<object>` | yes | Invoice line items. |
| `products[].name` | body | `string` | yes | Product or service name. |
| `products[].price` | body | `number` | yes | Product unit price. |
| `products[].quantity` | body | `number` | yes | Product quantity. |
| `products[].units` | body | `string` | yes | Units label. |
| `products[].vat_percentage` | body | `number` | no | VAT percentage for VAT invoice variants. |
| `series` | body | `string` | yes | Invoice series identifier. |
| `type` | body | `string` | yes | Invoice type enum observed from Finmei. |
| `use_default_seller_info` | body | `boolean` | yes | Whether to use the default seller information. |
