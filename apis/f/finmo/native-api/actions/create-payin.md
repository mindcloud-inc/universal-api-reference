# Create Payin with Finmo

Creates a new payin in Finmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/payin`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Create Payin](https://docs.finmo.net/reference/createpayin-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `currency` | body | `string` | yes |
| `payin_method_name` | body | `string` | yes |
| `payin_method_param` | body | `object` | yes |
| `redirect_url` | body | `string` | no |
| `advanced_redirect_url` | body | `object` | no |
| `fees_wallet_id` | body | `string` | no |
| `credit_wallet_id` | body | `string` | no |
| `payin_type` | body | `string` | no |
| `receipt_email` | body | `string` | no |
| `checkout_id` | body | `string` | no |
| `description` | body | `string` | no |
| `customer_id` | body | `string` | no |
| `organization_reference_id` | body | `string` | no |
| `metadata` | body | `object` | no |
| `expire_at` | body | `number` | no |
| `webhook_url` | body | `string` | no |
