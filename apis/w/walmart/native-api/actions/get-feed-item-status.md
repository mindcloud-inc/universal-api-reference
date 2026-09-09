# Get Feed Item Status with Walmart

Returns the overall feed status and item-level ingestion details for the specified feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/feeds/:feedId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Feed Item Status](https://developer.walmart.com/us-marketplace/reference/getallfeedstatuses#:~:text=Utilities-,All%20feed%20statuses,-GET)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDetails` | query | `boolean` | no | When true, includes detailed ingestion records for each item in the feed. |
| `feedId` | path | `string` | yes | A unique ID returned from the Bulk Upload API, used for tracking the feed file. |
