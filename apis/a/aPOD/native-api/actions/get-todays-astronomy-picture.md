# Get Today's Astronomy Picture with APOD

Retrieves today's APOD entry from NASA.

## Endpoint

- **Method:** `GET`
- **Path:** `/planetary/apod`
- **Base URL:** `https://api.nasa.gov`
- **Official documentation:** [Get Today's Astronomy Picture](https://api.nasa.gov/#apod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `thumbs` | query | `boolean` | no | Return a thumbnail URL when the APOD media is a video. |
