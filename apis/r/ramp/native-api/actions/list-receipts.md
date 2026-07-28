# List Receipts with Ramp

## Endpoint

- **Method:** `GET`
- **Path:** `receipts`
- **Base URL:** `https://api.ramp.com/developer/v1/`
- **Official documentation:** [List Receipts](https://docs.ramp.com/developer-api/v1/api/receipts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `foo` | query | `string` | no |
| `created_after` | query | `date` | no |
| `created_before` | query | `date` | no |
| `from_date` | query | `date` | no |
| `to_date` | query | `date` | no |
| `transaction_id` | query | `string` | no |
