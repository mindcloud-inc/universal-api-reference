# Create UTM Channel with Weberlo

Creates a UTM channel in Weberlo.

## Endpoint

- **Method:** `POST`
- **Path:** `/channel-utm`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [Create UTM Channel](https://developers.weberlo.com/#tag/UTM-Channel/paths/~1channel-utm/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | UTM channel name. |
| `icon` | body | `string` | yes | UTM channel icon URL. |
| `conditions[]` | body | `array<object>` | yes | UTM matching conditions array. |
