# List Collection Items with City of Tampa, Florida

Retrieves collection items from City of Tampa, Florida.

## Endpoint

- **Method:** `GET`
- **Path:** `https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items`
- **Base URL:** `https://www.tampa.gov`
- **Official documentation:** [List Collection Items](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Search API collection identifier, for example dataset. |
| `limit` | query | `number` | no | Maximum number of rows to return. |
| `offset` | query | `number` | no | Zero-based offset for paging through collection items. |
