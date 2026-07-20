# Create Feed in a Group with Adafruit IO

Creates a feed in an Adafruit IO group.

## Endpoint

- **Method:** `POST`
- **Path:** `/{username}/groups/:group_key/feeds`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Create Feed in a Group](https://io.adafruit.com/api/docs/#create-feed-in-a-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed` | body | `object` | yes |
| `group_key` | path | `string` | yes |
