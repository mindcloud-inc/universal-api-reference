# List Payins with Finmo

Retrieves payins from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/payin`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Payins](https://docs.finmo.net/reference/listallpayins-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `string` | no |
| `created_at` | query | `string` | no |
| `customer_id` | query | `string` | no |
| `credit_wallet_id` | query | `string` | no |
| `payin_method_name` | query | `string` | no |
| `start_time` | query | `number` | no |
| `end_time` | query | `number` | no |
| `limit` | query | `number` | no |
| `page` | query | `number` | no |
