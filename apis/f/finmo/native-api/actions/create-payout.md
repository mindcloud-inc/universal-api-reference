# Create Payout with Finmo

Creates a new payout in Finmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/payout`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Create Payout](https://docs.finmo.net/reference/createpayout-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sender_amount` | body | `number` | yes |
| `sender_currency` | body | `string` | yes |
| `sender_country` | body | `string` | no |
| `beneficiary_amount` | body | `number` | yes |
| `beneficiary_currency` | body | `string` | yes |
| `beneficiary_country` | body | `string` | no |
| `payout_method_name` | body | `string` | yes |
| `fx_rate_id` | body | `string` | no |
| `debit_wallet_id` | body | `string` | no |
| `fees_wallet_id` | body | `string` | no |
| `organization_reference_id` | body | `string` | no |
| `description` | body | `string` | no |
| `payout_method_param` | body | `object` | no |
| `payout_beneficiary_param` | body | `object` | no |
| `payout_controls` | body | `object` | no |
| `payout_beneficiary_id` | body | `string` | no |
| `payout_sender_id` | body | `string` | no |
| `payout_sender_param` | body | `object` | no |
| `purpose_code` | body | `string` | yes |
| `receipt_email` | body | `string` | no |
| `payout_reference` | body | `string` | no |
| `webhook_url` | body | `string` | no |
| `metadata` | body | `object` | no |
