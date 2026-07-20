# Create Hosted Payment Page with Invoice with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/request`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Hosted Payment Page with Invoice](https://support.paytabs.com/en/support/solutions/articles/60000929703-3-2-2-invoices-apis-initiating-creating-the-invoice-payment-request-via-payment-endpoint-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tran_type` | body | `string` | yes | PayTabs transaction type, usually sale. |
| `tran_class` | body | `string` | yes | PayTabs transaction class, usually ecom. |
| `cart_currency` | body | `string` | yes | Payment currency. |
| `cart_amount` | body | `number` | yes | Payment amount. |
| `cart_id` | body | `string` | yes | Unique merchant cart ID. |
| `cart_description` | body | `string` | yes | Cart description. |
| `invoice` | body | `object` | yes | Invoice object with at least line_items. |
| `callback` | body | `string` | yes | Callback URL. |
| `return` | body | `string` | yes | Return URL. |
