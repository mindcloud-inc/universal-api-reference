# List Refunds with Finmo

Retrieves refunds from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/refund`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Refunds](https://docs.finmo.net/reference/listallrefunds-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `string` | no |
| `payin_id` | query | `string` | no |
| `amount` | query | `number` | no |
| `created_at` | query | `string` | no |
| `start_time` | query | `number` | no |
| `end_time` | query | `number` | no |
| `limit` | query | `number` | no |
| `page` | query | `number` | no |
