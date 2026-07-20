# Create Payout Sender with Finmo

Creates a new payout sender in Finmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/payout-sender`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Create Payout Sender](https://docs.finmo.net/reference/createpayoutsender)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sender_name` | body | `string` | yes |
| `type` | body | `string` | yes |
| `description` | body | `string` | no |
| `metadata` | body | `object` | no |
| `email` | body | `string` | no |
| `organization_reference_id` | body | `string` | no |
| `address_line1` | body | `string` | no |
| `address_line2` | body | `string` | no |
| `address_city` | body | `string` | no |
| `address_state` | body | `string` | no |
| `address_country` | body | `string` | no |
| `address_zip_code` | body | `string` | no |
| `phone_number` | body | `string` | no |
| `phone_country_code` | body | `string` | no |
| `phone_number_e164` | body | `string` | no |
| `individual` | body | `object` | no |
| `company` | body | `object` | no |
