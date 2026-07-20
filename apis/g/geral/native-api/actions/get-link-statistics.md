# Get Link Statistics with Geral

Retrieves statistics for a link in Geral.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistics/:link_id`
- **Base URL:** `https://ger.al/api`
- **Official documentation:** [Get Link Statistics](https://ger.al/api-documentation/statistics)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link_id` | path | `number` | yes | The link ID to retrieve statistics for. |
| `start_date` | query | `string` | yes | Start date in Y-m-d format, for example 2026-04-01. |
| `end_date` | query | `string` | yes | End date in Y-m-d format, for example 2026-04-13. |
