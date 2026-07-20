# Get Astronomy Picture by Date with APOD

Retrieves an APOD entry from NASA by date.

## Endpoint

- **Method:** `GET`
- **Path:** `/planetary/apod`
- **Base URL:** `https://api.nasa.gov`
- **Official documentation:** [Get Astronomy Picture by Date](https://api.nasa.gov/#apod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | yes | Date of the APOD image to retrieve in YYYY-MM-DD format. |
| `thumbs` | query | `boolean` | no | Return a thumbnail URL when the APOD media is a video. |
