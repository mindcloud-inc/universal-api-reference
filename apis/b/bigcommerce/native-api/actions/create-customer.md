# Create Customer with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/customers`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `addresses[]` | body | `array<object>` | no | — |
| `phone` | body | `string` | no | — |
| `accepts_product_review_abandoned_cart_emails` | body | `boolean` | no | Format: `text`. |
| `company` | body | `string` | no | — |
