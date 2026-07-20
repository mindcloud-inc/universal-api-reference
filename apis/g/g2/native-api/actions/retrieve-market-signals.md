# Retrieve Market Signals with G2

Retrieves category buyer intent signals from G2 for a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/market_signals`
- **Base URL:** `https://data.g2.com`
- **Official documentation:** [Retrieve Market Signals](https://data.g2.com/openapi/v2.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_ids[]` | query | `string` | yes | Category IDs to scope market signals. |
| `end_date` | query | `date` | no | End date for the market signals range. |
| `start_date` | query | `date` | no | Start date for the market signals range. |
