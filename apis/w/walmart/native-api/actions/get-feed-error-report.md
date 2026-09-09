# Get Feed Error Report with Walmart

Download a detailed error report for a submitted feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/feeds/:feedId/errorReport`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Feed Error Report](https://developer.walmart.com/us-marketplace/reference/getallfeedstatuses#:~:text=Utilities-,All%20feed%20statuses,-GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `list<string>` | yes | When true, includes detailed ingestion records for each item in the feed. |
| `feedId` | path | `string` | yes | A unique ID returned from the Bulk Upload API, used for tracking the feed file. |
