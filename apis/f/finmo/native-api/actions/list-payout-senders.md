# List Payout Senders with Finmo

Retrieves payout senders from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/payout-sender`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Payout Senders](https://docs.finmo.net/reference/getallpayoutsender)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payout_sender_id` | query | `string` | no |
| `type` | query | `string` | no |
| `sender_name` | query | `string` | no |
| `email` | query | `string` | no |
| `organization_reference_id` | query | `string` | no |
| `address_line1` | query | `string` | no |
| `address_line2` | query | `string` | no |
| `address_city` | query | `string` | no |
| `address_state` | query | `string` | no |
| `address_country` | query | `string` | no |
| `address_zip_code` | query | `string` | no |
| `phone_number` | query | `string` | no |
| `phone_country_code` | query | `string` | no |
| `phone_number_e164` | query | `string` | no |
| `description` | query | `string` | no |
| `is_active` | query | `boolean` | no |
| `created_at` | query | `string` | no |
| `limit` | query | `number` | no |
| `page` | query | `number` | no |
