# Get Playlist with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/playlists/:plid`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Playlist](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Playlist page number. |
| `plid` | path | `string` | yes | Playlist ID. |
