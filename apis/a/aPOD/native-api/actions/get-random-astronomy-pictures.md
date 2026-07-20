# Get Random Astronomy Pictures with APOD

Retrieves random APOD entries from NASA.

## Endpoint

- **Method:** `GET`
- **Path:** `/planetary/apod`
- **Base URL:** `https://api.nasa.gov`
- **Official documentation:** [Get Random Astronomy Pictures](https://api.nasa.gov/#apod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | yes | Number of random APOD images to retrieve. NASA allows positive integers up to 100. |
| `thumbs` | query | `boolean` | no | Return thumbnail URLs when APOD media entries are videos. |
