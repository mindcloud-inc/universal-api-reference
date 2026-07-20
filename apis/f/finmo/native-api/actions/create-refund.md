# Create Refund with Finmo

Creates a new refund in Finmo.

## Endpoint

- **Method:** `POST`
- **Path:** `/refund`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [Create Refund](https://docs.finmo.net/reference/createrefund-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payin_id` | body | `string` | yes |
| `type` | body | `string` | yes |
| `amount` | body | `number` | no |
| `currency` | body | `string` | no |
| `organization_reference_id` | body | `string` | no |
| `webhook_url` | body | `string` | no |
| `metadata` | body | `object` | no |
