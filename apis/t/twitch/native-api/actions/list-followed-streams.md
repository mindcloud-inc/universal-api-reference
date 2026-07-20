# List Followed Streams with Twitch

Retrieves followed live streams from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/streams/followed`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Followed Streams](https://dev.twitch.tv/docs/api/reference#get-followed-streams)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `string` | yes | The ID of the user whose followed live streams you want to get. |
| `first` | query | `number` | no | The maximum number of items to return per page. |
| `after` | query | `string` | no | The cursor used to get the next page of results. |
