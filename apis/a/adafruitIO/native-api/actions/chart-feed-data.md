# Chart Feed Data with Adafruit IO

Retrieves charted data from an Adafruit IO feed.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/feeds/:feed_key/data/chart`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Chart Feed Data](https://io.adafruit.com/api/docs/#chart-feed-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_time` | query | `date` | no |
| `feed_key` | path | `string` | yes |
| `field` | query | `string` | no |
| `hours` | query | `number` | no |
| `raw` | query | `boolean` | no |
| `resolution` | query | `number` | no |
| `start_time` | query | `date` | no |
