# Get Predictions By Stop ID with NextBus

Retrieves stop predictions from NextBus by stop ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/publicXMLFeed`
- **Base URL:** `https://retro.umoiq.com/service`
- **Official documentation:** [Get Predictions By Stop ID](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=14)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `a` | query | `string` | yes |
| `stopId` | query | `string` | yes |
