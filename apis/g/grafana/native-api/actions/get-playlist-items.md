# Get Playlist Items with Grafana

Retrieves playlist items from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/playlists/:uid/items`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Playlist Items](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/playlist/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The playlist UID. |
