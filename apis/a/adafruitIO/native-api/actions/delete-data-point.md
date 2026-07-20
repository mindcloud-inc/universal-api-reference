# Delete Data Point with Adafruit IO

Deletes a data point from an Adafruit IO feed.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/{username}/feeds/:feed_key/data/:id`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Delete Data Point](https://io.adafruit.com/api/docs/#delete-data-point)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | path | `string` | yes |
| `id` | path | `string` | yes |
