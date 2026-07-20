# Patch Invoice with Finmei

## Endpoint

- **Method:** `PATCH`
- **Path:** `/invoices/:invoiceId`
- **Base URL:** `https://app.finmei.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buyer` | body | `object` | no | Buyer object. |
| `buyer.country` | body | `string` | no | Buyer country code. |
| `buyer.first_name` | body | `string` | no | Buyer first name. |
| `buyer.last_name` | body | `string` | no | Buyer last name. |
| `buyer.type` | body | `string` | no | Buyer type. |
| `currency` | body | `string` | no | Invoice currency code. |
| `invoice_date` | body | `date` | no | Invoice issue date. |
| `invoiceId` | path | `string` | yes | — |
| `products` | body | `list<object>` | no | Invoice line items. |
| `products[].name` | body | `string` | no | Product or service name. |
| `products[].price` | body | `number` | no | Product unit price. |
| `products[].quantity` | body | `number` | no | Product quantity. |
| `products[].units` | body | `string` | no | Units label. |
| `products[].vat_percentage` | body | `number` | no | VAT percentage for VAT invoice variants. |
| `series` | body | `string` | no | Invoice series identifier. |
| `type` | body | `string` | no | Invoice type enum observed from Finmei. |
| `use_default_seller_info` | body | `boolean` | no | Whether to use the default seller information. |
