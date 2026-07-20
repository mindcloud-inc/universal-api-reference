# List Channels with Pusher

Retrieves channels from Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/{appId}/channels`
- **Base URL:** `https://api-{cluster}.pusher.com`
- **Official documentation:** [List Channels](https://pusher.com/docs/channels/library_auth_reference/rest-api/#get-channels-fetch-info-for-multiple-channels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_by_prefix` | query | `string` | no | Return only channels whose names start with the provided prefix. |
| `info` | query | `string` | no | Comma-separated channel attributes to include in the response, such as user_count. |
