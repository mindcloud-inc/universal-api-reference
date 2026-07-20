# Get Channel with Pusher

Retrieves channel details from Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/{appId}/channels/:channel_name`
- **Base URL:** `https://api-{cluster}.pusher.com`
- **Official documentation:** [Get Channel](https://pusher.com/docs/channels/library_auth_reference/rest-api/#get-channel-fetch-info-for-one-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_name` | path | `string` | yes | The name of the channel to inspect. |
| `info` | query | `string` | no | Comma-separated channel attributes to include, such as user_count or subscription_count. |
