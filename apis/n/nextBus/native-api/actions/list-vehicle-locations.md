# List Vehicle Locations with NextBus

Retrieves changed vehicle locations from NextBus.

## Endpoint

- **Method:** `GET`
- **Path:** `/publicXMLFeed`
- **Base URL:** `https://retro.umoiq.com/service`
- **Official documentation:** [List Vehicle Locations](https://retro.umoiq.com/xmlFeedDocs/NextBusXMLFeed.pdf#page=20)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `a` | query | `string` | yes | — |
| `r` | query | `string` | yes | — |
| `t` | query | `string` | yes | Last returned vehicle location timestamp in milliseconds since epoch. Use 0 for recent vehicles. |
