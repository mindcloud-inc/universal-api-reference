# Get Last Data with Adafruit IO

Retrieves the last data point from an Adafruit IO feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data/last`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Get Last Data](https://io.adafruit.com/api/docs/#get-last-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | path | `string` | yes |
