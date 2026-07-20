# Create Payment Request with GoAffPro

Creates a new payment request in GoAffPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/payments/requests`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Create Payment Request](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | body | `number` | yes | ID of the affiliate making the payment request. |
| `tx_ids[]` | body | `array<number>` | yes | Transaction IDs to include in the payment request. |
| `note` | body | `string` | no | Optional note for the payment request. |
| `invoice_url` | body | `string` | no | Optional invoice URL for the payment request. |
