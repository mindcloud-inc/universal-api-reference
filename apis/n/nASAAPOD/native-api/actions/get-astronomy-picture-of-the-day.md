# Get Astronomy Picture of the Day with NASA APOD

## Endpoint

- **Method:** `GET`
- **Path:** `/planetary/apod`
- **Base URL:** `https://api.nasa.gov`
- **Official documentation:** [Get Astronomy Picture of the Day](https://api.nasa.gov/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | no | Optional APOD date in YYYY-MM-DD. Leave empty for today. |
| `thumbs` | query | `boolean` | no | When true, NASA includes thumbnail_url for video APODs. |
