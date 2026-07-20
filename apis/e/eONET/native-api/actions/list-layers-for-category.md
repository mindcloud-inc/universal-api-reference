# List Layers for Category with EONET

Retrieves layers for a category from EONET.

## Endpoint

- **Method:** `GET`
- **Path:** `/layers/:categoryId`
- **Base URL:** `https://eonet.gsfc.nasa.gov/api/v3`
- **Official documentation:** [List Layers for Category](https://eonet.gsfc.nasa.gov/docs/v3#layers-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | Category ID such as wildfires or volcanoes. |
