# Replace Action with Adafruit IO

Replaces an action in Adafruit IO.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{username}/actions/:id`
- **Base URL:** `https://io.adafruit.com/api/v2`
- **Official documentation:** [Replace Action](https://io.adafruit.com/api/docs/#replace-action)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `trigger` | body | `object` | yes |
