# Create Data with Adafruit IO

Creates a data point in an Adafruit IO feed.

## Endpoint

- **Method:** `POST`
- **Path:** `/{username}/feeds/:feed_key/data`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Create Data](https://io.adafruit.com/api/docs/#create-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `created_at` | body | `date` | no |
| `ele` | body | `number` | no |
| `feed_key` | path | `string` | yes |
| `lat` | body | `number` | no |
| `lon` | body | `number` | no |
| `value` | body | `string` | yes |
