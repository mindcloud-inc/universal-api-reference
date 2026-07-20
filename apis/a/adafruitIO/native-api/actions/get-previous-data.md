# Get Previous Data with Adafruit IO

Retrieves the previous data point from an Adafruit IO feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data/previous`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Get Previous Data](https://io.adafruit.com/api/docs/#get-previous-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | path | `string` | yes |
| `include` | query | `string` | no |
