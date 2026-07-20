# Get Collection Item with City of Tampa, Florida

Retrieves a collection item from City of Tampa, Florida.

## Endpoint

- **Method:** `GET`
- **Path:** `https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items/:itemId`
- **Base URL:** `https://www.tampa.gov`
- **Official documentation:** [Get Collection Item](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Search API collection identifier, for example dataset. |
| `itemId` | path | `string` | yes | GeoHub item identifier. |
