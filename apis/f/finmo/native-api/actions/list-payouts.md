# List Payouts with Finmo

Retrieves payouts from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/payout`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Payouts](https://docs.finmo.net/reference/listallpayouts-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `string` | no |
| `payout_method_name` | query | `string` | no |
| `created_at` | query | `string` | no |
| `start_time` | query | `number` | no |
| `end_time` | query | `number` | no |
| `limit` | query | `number` | no |
| `page` | query | `number` | no |
