# List Connected Records with City of Tampa, Florida

Retrieves connected records from City of Tampa, Florida.

## Endpoint

- **Method:** `GET`
- **Path:** `https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items/:recordId/connected`
- **Base URL:** `https://www.tampa.gov`
- **Official documentation:** [List Connected Records](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Search API collection identifier, for example dataset. |
| `recordId` | path | `string` | yes | GeoHub record identifier. |
