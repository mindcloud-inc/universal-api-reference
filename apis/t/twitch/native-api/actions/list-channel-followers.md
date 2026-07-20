# List Channel Followers with Twitch

Retrieves channel follower records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/followers`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Channel Followers](https://dev.twitch.tv/docs/api/reference#get-channel-followers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The broadcaster’s ID. |
| `user_id` | query | `string` | no | A user’s ID used to check whether they follow the broadcaster. |
| `first` | query | `number` | no | The maximum number of items to return per page. |
| `after` | query | `string` | no | The cursor used to get the next page of results. |
