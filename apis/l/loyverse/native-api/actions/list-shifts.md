# List Shifts with Loyverse

Retrieves shift records from the Loyverse account.

## Endpoint

- **Method:** `GET`
- **Path:** `/shifts`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Shifts](https://developer.loyverse.com/docs/#tag/Shifts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store_ids` | query | `string` | no | A comma-separated list of store ids to filter shifts |
| `created_at_min` | query | `date` | no | Show shifts opened after date (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `created_at_max` | query | `date` | no | Show shifts opened before date (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `limit` | query | `number` | no | Used for pagination |
| `cursor` | query | `string` | no | Used for pagination |
