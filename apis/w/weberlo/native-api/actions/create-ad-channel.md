# Create Ad Channel with Weberlo

Creates an ad channel in Weberlo.

## Endpoint

- **Method:** `POST`
- **Path:** `/channel-ad`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [Create Ad Channel](https://developers.weberlo.com/#tag/Ad-Channels/paths/~1channel-ad/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Ad channel name. |
| `icon` | body | `string` | yes | Ad channel icon URL. |
| `ad_platform` | body | `string` | yes | Ad platform identifier. |
| `ad_account_id` | body | `string` | yes | Ad account ID. |
