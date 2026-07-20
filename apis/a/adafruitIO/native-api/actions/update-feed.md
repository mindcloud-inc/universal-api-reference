# Update Feed with Adafruit IO

Updates an existing feed in Adafruit IO.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{username}/feeds/:feed_key`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Update Feed](https://io.adafruit.com/api/docs/#update-feed)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed` | body | `object` | yes |
| `feed_key` | path | `string` | yes |
