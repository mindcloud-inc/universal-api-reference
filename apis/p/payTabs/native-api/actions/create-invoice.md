# Create Invoice with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/new/invoice`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Invoice](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Invoices-APIs/Invoices-Step-3-Initiating-the-payment/Invoices-Step-3-Initiating-the-payment-Landing/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tran_type` | body | `string` | yes | PayTabs transaction type, usually sale. |
| `tran_class` | body | `string` | yes | PayTabs transaction class, usually ecom. |
| `cart_currency` | body | `string` | yes | Invoice cart currency, for example AED. |
| `cart_amount` | body | `number` | yes | Invoice cart amount. |
| `cart_id` | body | `string` | yes | Unique merchant cart ID. |
| `cart_description` | body | `string` | yes | Invoice/cart description. |
| `hide_shipping` | body | `boolean` | yes | Whether to hide shipping details. |
| `customer_ref` | body | `string` | yes | Customer reference. |
| `customer_details` | body | `object` | yes | Customer details object. |
| `invoice` | body | `object` | yes | Invoice details object including line items. |
