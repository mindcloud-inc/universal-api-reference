# Get all transactions with Lunch Money

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Get all transactions](https://alpha.lunchmoney.dev/v2/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | query | `string` | no |
| `end_date` | query | `string` | no |
| `include_files` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
