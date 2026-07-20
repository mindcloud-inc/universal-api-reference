# List Tagged Visitors with GoSquared

Retrieves tagged visitors for a GoSquared site.

## Endpoint

- **Method:** `GET`
- **Path:** `account/v1/taggedVisitors`
- **Base URL:** `https://api.gosquared.com`
- **Official documentation:** [List Tagged Visitors](https://www.gosquared.com/docs/account/taggedVisitors/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presenter` | query | `string` | no | Modifies the response data structure. Accepted values: plain, indexed. |
