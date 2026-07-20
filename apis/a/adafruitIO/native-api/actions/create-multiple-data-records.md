# Create Multiple Data Records with Adafruit IO

Creates multiple data points in an Adafruit IO feed.

## Endpoint

- **Method:** `POST`
- **Path:** `/{username}/feeds/:feed_key/data/batch`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Create Multiple Data Records](https://io.adafruit.com/api/docs/#create-multiple-data-records)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes |
| `feed_key` | path | `string` | yes |
