# Get Most Recent Data with Adafruit IO

Retrieves the most recent feed data from Adafruit IO in CSV format.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data/retain`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Get Most Recent Data](https://io.adafruit.com/api/docs/#get-most-recent-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | path | `string` | yes |
