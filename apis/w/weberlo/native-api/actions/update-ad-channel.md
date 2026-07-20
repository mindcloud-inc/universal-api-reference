# Update Ad Channel with Weberlo

Updates an ad channel in Weberlo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/channel-ad/:id`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [Update Ad Channel](https://developers.weberlo.com/#tag/Ad-Channels/paths/~1channel-ad~1{id}/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ad channel ID. |
| `name` | body | `string` | no | Updated ad channel name. |
| `icon` | body | `string` | no | Updated ad channel icon URL. |
