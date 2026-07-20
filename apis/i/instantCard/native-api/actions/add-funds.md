# Add Funds with InstantCard

Adds funds to an InstantCard organization balance.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/organizations/:organizationId/add_funds`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Add Funds](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_address2` | query | `string` | no | Billing address line 2. |
| `channel` | query | `string` | no | Payment channel. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
| `amount` | query | `string` | yes | Amount to add. |
| `number` | query | `string` | yes | Credit card number. |
| `exp_month` | query | `string` | yes | Card expiration month. |
| `exp_year` | query | `string` | yes | Card expiration year. |
| `cvc` | query | `string` | yes | Card security code. |
| `full_name` | query | `string` | yes | Cardholder full name. |
| `billing_address1` | query | `string` | yes | Billing address line 1. |
| `billing_country` | query | `string` | yes | Billing country. |
| `billing_city` | query | `string` | yes | Billing city. |
| `billing_state` | query | `string` | yes | Billing state. |
| `billing_zip_code` | query | `string` | yes | Billing postal code. |
