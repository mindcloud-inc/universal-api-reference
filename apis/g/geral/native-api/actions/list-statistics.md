# List Statistics with Geral

Retrieves account statistics from Geral.

## Endpoint

- **Method:** `GET`
- **Path:** `/statistics/`
- **Base URL:** `https://ger.al/api`
- **Official documentation:** [List Statistics](https://ger.al/api-documentation/statistics)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date in Y-m-d format, for example 2026-04-01. |
| `end_date` | query | `string` | yes | End date in Y-m-d format, for example 2026-04-13. |
