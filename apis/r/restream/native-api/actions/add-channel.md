# Add Channel with Restream

Creates a streaming channel in Restream.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/channels`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [Add Channel](https://developers.restream.io/channels/channel-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platformId` | body | `number` | yes | Platform ID from Restream's platform list. |
| `streamKey` | body | `string` | no | Stream key, required for some platforms. |
| `streamUrl` | body | `string` | no | Stream URL, required for some platforms. |
