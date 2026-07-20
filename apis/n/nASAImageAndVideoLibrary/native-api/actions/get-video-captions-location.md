# Get Video Captions Location with NASA Image and Video Library

Retrieves a video captions URL from NASA Image and Video Library.

## Endpoint

- **Method:** `GET`
- **Path:** `/captions/:nasa_id`
- **Base URL:** `https://images-api.nasa.gov`
- **Official documentation:** [Get Video Captions Location](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nasa_id` | path | `string` | yes | The NASA video asset ID whose captions location to retrieve. |
