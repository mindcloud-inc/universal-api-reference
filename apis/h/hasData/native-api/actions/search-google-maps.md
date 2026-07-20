# Search Google Maps with HasData

Retrieves Google Maps search results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google-maps/search`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Google Maps](https://docs.hasdata.com/apis/google-maps/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ll` | query | `string` | no | Map coordinates in the format @lat,lng,zoomz. |
| `q` | query | `string` | yes | Search query for Google Maps. |
| `start` | query | `number` | no | Result offset for pagination. |
