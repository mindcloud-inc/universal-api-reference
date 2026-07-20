# Get Data Point with Adafruit IO

Retrieves a data point from an Adafruit IO feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data/:id`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Get Data Point](https://io.adafruit.com/api/docs/#get-data-point)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | path | `string` | yes |
| `id` | path | `string` | yes |
| `include` | query | `string` | no |
