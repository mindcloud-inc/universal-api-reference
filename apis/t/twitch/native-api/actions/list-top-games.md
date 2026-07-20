# List Top Games with Twitch

Retrieves top game categories from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/games/top`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Top Games](https://dev.twitch.tv/docs/api/reference#get-top-games)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first` | query | `number` | no | The maximum number of objects to return. Maximum: 100. Default: 20. |
| `after` | query | `string` | no | The cursor used to get the next page of results. |
| `before` | query | `string` | no | The cursor used to get the previous page of results. |
