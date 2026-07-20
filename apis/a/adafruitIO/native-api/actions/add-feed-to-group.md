# Add Feed to Group with Adafruit IO

Adds a feed to an Adafruit IO group.

## Endpoint

- **Method:** `POST`
- **Path:** `/{username}/groups/:group_key/add`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Add Feed to Group](https://io.adafruit.com/api/docs/#add-feed-to-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | query | `string` | yes |
| `group_key` | path | `string` | yes |
