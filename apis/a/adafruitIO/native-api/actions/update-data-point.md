# Update Data Point with Adafruit IO

Updates a data point in an Adafruit IO feed.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{username}/feeds/:feed_key/data/:id`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Update Data Point](https://io.adafruit.com/api/docs/#update-data-point)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `created_at` | body | `date` | no |
| `ele` | body | `number` | no |
| `feed_key` | path | `string` | yes |
| `id` | path | `string` | yes |
| `lat` | body | `number` | no |
| `lon` | body | `number` | no |
| `value` | body | `string` | yes |
