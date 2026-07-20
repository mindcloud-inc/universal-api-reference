# List Streams with Twitch

Retrieves live stream records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/streams`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Streams](https://dev.twitch.tv/docs/api/reference#get-streams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `string` | no | A user ID used to filter the list of streams. Specify this parameter up to 100 times. Send multiple values as a array. |
| `user_login` | query | `string` | no | A user login name used to filter the list of streams. Specify this parameter up to 100 times. Send multiple values as a array. |
| `game_id` | query | `string` | no | A game ID used to filter the list of streams. Specify this parameter up to 100 times. Send multiple values as a array. |
| `type` | query | `list` | no | A stream type used to filter the list of streams. Accepted values: `all`, `live`. |
| `language` | query | `string` | no | A language used to filter the list of streams. |
| `first` | query | `number` | no | The maximum number of objects to return. Maximum: 100. Default: 20. |
| `after` | query | `string` | no | The cursor used to get the next page of results. |
| `before` | query | `string` | no | The cursor used to get the previous page of results. |
