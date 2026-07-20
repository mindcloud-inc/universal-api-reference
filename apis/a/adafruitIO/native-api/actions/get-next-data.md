# Get Next Data with Adafruit IO

Retrieves the next data point from an Adafruit IO feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data/next`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Get Next Data](https://io.adafruit.com/api/docs/#get-next-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | path | `string` | yes |
| `include` | query | `string` | no |
