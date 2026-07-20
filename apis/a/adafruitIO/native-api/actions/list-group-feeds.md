# List Group Feeds with Adafruit IO

Retrieves feeds from an Adafruit IO group.

## Endpoint

- **Method:** `GET`
- **Path:** `/{username}/groups/:group_key/feeds`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [List Group Feeds](https://io.adafruit.com/api/docs/#get-group-feeds)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_key` | path | `string` | yes |
