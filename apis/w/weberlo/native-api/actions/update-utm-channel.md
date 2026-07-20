# Update UTM Channel with Weberlo

Updates a UTM channel in Weberlo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/channel-utm/:id`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [Update UTM Channel](https://developers.weberlo.com/#tag/UTM-Channel/paths/~1channel-utm~1{id}/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UTM channel ID. |
| `name` | body | `string` | no | Updated UTM channel name. |
| `icon` | body | `string` | no | Updated UTM channel icon URL. |
| `conditions[]` | body | `array<object>` | no | Updated UTM matching conditions array. |
