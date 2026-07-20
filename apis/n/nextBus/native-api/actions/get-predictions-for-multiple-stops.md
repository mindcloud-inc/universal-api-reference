# Get Predictions For Multiple Stops with NextBus

Retrieves stop predictions from NextBus for multiple stops.

## Endpoint

- **Method:** `GET`
- **Path:** `/publicXMLFeed`
- **Base URL:** `https://retro.umoiq.com/service`
- **Official documentation:** [Get Predictions For Multiple Stops](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `a` | query | `string` | yes | — |
| `stops` | query | `string` | yes | Route tag and stop tag joined with a pipe, for example 01\|gtc_d. |
