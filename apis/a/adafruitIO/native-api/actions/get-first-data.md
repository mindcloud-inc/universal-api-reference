# Get First Data with Adafruit IO

Retrieves the first data point from an Adafruit IO feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data/first`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Get First Data](https://io.adafruit.com/api/docs/#get-first-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | path | `string` | yes |
| `include` | query | `string` | no |
