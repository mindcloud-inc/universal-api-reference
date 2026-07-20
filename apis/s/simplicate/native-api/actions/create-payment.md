# Create Payment with Simplicate

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/payment`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Create Payment](https://developer.simplicate.com/docs/api/v2/reference/create-invoices-payment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | no | Payment amount. |
| `date` | body | `string` | no | Payment date in YYYY-MM-DD format. |
| `description` | body | `string` | no | Payment description. |
| `invoice_id` | body | `string` | no | Invoice identifier. |
