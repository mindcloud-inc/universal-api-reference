# Remove Feed from Group with Adafruit IO

Removes a feed from an Adafruit IO group.

## Endpoint

- **Method:** `POST`
- **Path:** `/{username}/groups/:group_key/remove`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Remove Feed from Group](https://io.adafruit.com/api/docs/#remove-feed-from-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feed_key` | query | `string` | yes |
| `group_key` | path | `string` | yes |
