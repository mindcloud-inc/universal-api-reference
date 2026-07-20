# Update Group with Adafruit IO

Updates an existing group in Adafruit IO.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{username}/groups/:group_key`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Update Group](https://io.adafruit.com/api/docs/#update-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group` | body | `object` | yes |
| `group_key` | path | `string` | yes |
