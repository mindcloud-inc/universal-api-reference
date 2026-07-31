# Get APOD Date Range with NASA APOD

## Endpoint

- **Method:** `GET`
- **Path:** `/planetary/apod`
- **Base URL:** `https://api.nasa.gov`
- **Official documentation:** [Get APOD Date Range](https://api.nasa.gov/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | yes | First APOD date in YYYY-MM-DD. |
| `end_date` | query | `date` | no | Optional last APOD date in YYYY-MM-DD. NASA defaults it to today. |
| `thumbs` | query | `boolean` | no | When true, NASA includes thumbnail_url for video APODs. |
