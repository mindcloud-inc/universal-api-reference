# Create Invoice with Poof

Creates a new fiat invoice in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.poof.io/api/v1/create_fiat_invoice`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Create Invoice](https://docs.poof.io/reference/createinvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | yes | Invoice amount. |
| `payment` | body | `string` | yes | Fiat payment method. |
| `currency` | body | `string` | yes | Fiat currency code. |
| `redirect_url` | body | `string` | yes | Redirect URL. |
| `success_url` | body | `string` | yes | Success URL. |
