# Create Billing Request with GoCardless

Creates a new billing request in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing_requests`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Create Billing Request](https://developer.gocardless.com/api-reference/#billing-requests-create-a-billing-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_request` | body | `object` | no | Payment request payload for the billing request. |
| `payment_request.description` | body | `string` | no | Human-readable description displayed to the payer. |
| `payment_request.amount` | body | `number` | no | Amount in minor units. |
| `payment_request.currency` | body | `list<string>` | no | ISO 4217 currency code for the payment request. Accepted values: `0`, `1`. |
| `mandate_request` | body | `object` | no | Mandate request payload for the billing request. |
| `mandate_request.scheme` | body | `list<string>` | no | Bank payment scheme for the mandate request. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `mandate_request.verify` | body | `list<string>` | no | Verification preference for the mandate request. Accepted values: `0`, `1`, `2`, `3`. |
| `links` | body | `object` | no | Related resource identifiers for this billing request. |
| `links.customer` | body | `string` | no | ID of the customer against which this request should be made. |
| `links.customer_bank_account` | body | `string` | no | ID of the customer bank account against which this request should be made. |
| `links.creditor` | body | `string` | no | ID of the associated creditor. |
| `fallback_enabled` | body | `boolean` | no | If true, this billing request can fallback from instant payment to direct debit. |
| `metadata` | body | `object` | no | Key-value store of custom data. |
