# Process Custom POST Request with Automatic Data Extraction

Processes a custom POST request in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Process Custom POST Request](https://docs.zyte.com/zyte-api/usage/reference.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
