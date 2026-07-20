# Create Payment with GoCardless

Creates a new payment in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Create Payment](https://developer.gocardless.com/api-reference/#payments-create-a-payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `currency` | body | `string` | yes |
| `links[mandate]` | body | `string` | yes |
| `charge_date` | body | `date` | no |
| `description` | body | `string` | no |
| `reference` | body | `string` | no |
| `app_fee` | body | `number` | no |
| `faster_ach` | body | `boolean` | no |
| `retry_if_possible` | body | `boolean` | no |
| `psu_interaction_type` | body | `string` | no |
| `metadata` | body | `object` | no |
