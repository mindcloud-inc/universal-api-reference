# List Feed Data with Adafruit IO

Retrieves data points from an Adafruit IO feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [List Feed Data](https://io.adafruit.com/api/docs/#get-feed-data)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_time` | query | `date` | no |
| `feed_key` | path | `string` | yes |
| `start_time` | query | `date` | no |
