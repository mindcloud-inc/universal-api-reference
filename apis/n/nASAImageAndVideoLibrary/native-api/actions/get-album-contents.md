# Get Album Contents with NASA Image and Video Library

Retrieves album contents from NASA Image and Video Library.

## Endpoint

- **Method:** `GET`
- **Path:** `/album/:album_name`
- **Base URL:** `https://images-api.nasa.gov`
- **Official documentation:** [Get Album Contents](https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `album_name` | path | `string` | yes | The case-sensitive NASA album name to retrieve. |
| `page` | query | `number` | no | Page number to retrieve. Starts at 1. |
