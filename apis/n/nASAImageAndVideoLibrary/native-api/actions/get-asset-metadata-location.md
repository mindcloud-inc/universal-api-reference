# Get Asset Metadata Location with NASA Image and Video Library

Retrieves an asset metadata URL from NASA Image and Video Library.

## Endpoint

- **Method:** `GET`
- **Path:** `/metadata/:nasa_id`
- **Base URL:** `https://images-api.nasa.gov`
- **Official documentation:** [Get Asset Metadata Location](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nasa_id` | path | `string` | yes | The NASA media asset ID whose metadata location to retrieve. |
