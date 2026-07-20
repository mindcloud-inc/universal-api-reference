# Get Predictions By Stop ID And Route with NextBus

Retrieves stop predictions from NextBus by stop ID and route.

## Endpoint

- **Method:** `GET`
- **Path:** `/publicXMLFeed`
- **Base URL:** `https://retro.umoiq.com/service`
- **Official documentation:** [Get Predictions By Stop ID And Route](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=14)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `a` | query | `string` | yes |
| `stopId` | query | `string` | yes |
| `routeTag` | query | `string` | yes |
