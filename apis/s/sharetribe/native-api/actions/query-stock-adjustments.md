# Query Stock Adjustments with Sharetribe

Retrieves stock adjustments from Sharetribe.

## Endpoint

- **Method:** `GET`
- **Path:** `stock_adjustments/query`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Query Stock Adjustments](https://www.sharetribe.com/api-reference/integration.html#query-stock-adjustments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listingId` | query | `string` | yes | The ID of the listing. |
| `start` | query | `date` | yes | Filter stock adjustments at or after this ISO 8601 timestamp. |
| `end` | query | `date` | yes | Filter stock adjustments before this ISO 8601 timestamp. |
