# List Payout Beneficiaries with Finmo

Retrieves payout beneficiaries from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/payout-beneficiary`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Payout Beneficiaries](https://docs.finmo.net/reference/getallpayoutbeneficiary-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | query | `string` | no |
| `include_deleted` | query | `boolean` | no |
| `created_at` | query | `string` | no |
| `start_time` | query | `number` | no |
| `end_time` | query | `number` | no |
| `limit` | query | `number` | no |
| `page` | query | `number` | no |
