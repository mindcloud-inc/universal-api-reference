# Post Buyer Payment Details with Escrow.com

Submits buyer payment details in Escrow.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction/:transaction_id/buyer_payment`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Post Buyer Payment Details](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_name` | body | `string` | no | Name on the buyer bank account. |
| `bank_name` | body | `string` | no | Name of the buyer's bank. |
| `bank_state` | body | `string` | no | State or province for the buyer's bank. |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
| `bank_country` | body | `string` | no | Two-letter country code for the buyer's bank when paying by wire. |
