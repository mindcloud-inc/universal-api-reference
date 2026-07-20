# List Clips with Twitch

Retrieves clip records and metadata from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/clips`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Clips](https://dev.twitch.tv/docs/api/reference#get-clips)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | no | An ID that identifies the broadcaster whose video clips you want to get. |
| `game_id` | query | `string` | no | An ID that identifies the game whose clips you want to get. |
| `id` | query | `string` | no | An ID that identifies the clip to get. Include this parameter for each clip you want to fetch. Send multiple values as a array. |
| `started_at` | query | `date` | no | The start date used to filter clips. Specify the date and time in RFC3339 format. |
| `ended_at` | query | `date` | no | The end date used to filter clips. If omitted, Twitch uses one week after the start date. |
| `first` | query | `number` | no | The maximum number of clips to return per page. Minimum 1, maximum 100. |
| `after` | query | `string` | no | The cursor used to get the next page of results. |
| `before` | query | `string` | no | The cursor used to get the previous page of results. |
| `is_featured` | query | `boolean` | no | Whether to return only featured clips. |
