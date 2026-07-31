# Get Random APODs with NASA APOD

## Endpoint

- **Method:** `GET`
- **Path:** `/planetary/apod`
- **Base URL:** `https://api.nasa.gov`
- **Official documentation:** [Get Random APODs](https://api.nasa.gov/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of randomly selected APODs. Maximum length: 100. |
| `thumbs` | query | `boolean` | no | When true, NASA includes thumbnail_url for video APODs. |
