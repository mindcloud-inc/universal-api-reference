# Create Mandate with GoCardless

Creates a new mandate in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/mandates`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Create Mandate](https://developer.gocardless.com/api-reference/#mandates-create-a-mandate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorisation_source` | body | `list` | no | Accepted values: `0`, `1`, `2`. |
| `payer_ip_address` | body | `string` | no | — |
| `reference` | body | `string` | no | — |
| `scheme` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
| `links` | body | `object` | no | — |
| `links.customer_bank_account` | body | `string` | yes | — |
| `links.creditor` | body | `string` | no | — |
