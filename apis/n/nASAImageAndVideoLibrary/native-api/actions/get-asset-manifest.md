# Get Asset Manifest with NASA Image and Video Library

Retrieves an asset manifest from NASA Image and Video Library.

## Endpoint

- **Method:** `GET`
- **Path:** `/asset/:nasa_id`
- **Base URL:** `https://images-api.nasa.gov`
- **Official documentation:** [Get Asset Manifest](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nasa_id` | path | `string` | yes | The NASA media asset ID to retrieve. |
