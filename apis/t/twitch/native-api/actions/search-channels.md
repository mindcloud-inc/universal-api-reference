# Search Channels with Twitch

Searches Twitch channels using a query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/channels`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Search Channels](https://dev.twitch.tv/docs/api/reference#search-channels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The URI-encoded search string. This may contain a maximum of 100 characters. |
| `live_only` | query | `boolean` | no | A Boolean value that determines whether the response includes only channels that are currently streaming live. |
| `first` | query | `number` | no | The maximum number of objects to return. Maximum: 100. Default: 20. |
| `after` | query | `string` | no | The cursor used to get the next page of results. |
