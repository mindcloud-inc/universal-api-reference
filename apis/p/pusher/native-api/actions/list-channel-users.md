# List Channel Users with Pusher

Retrieves users from a Pusher presence channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/{appId}/channels/:channel_name/users`
- **Base URL:** `https://api-{cluster}.pusher.com`
- **Official documentation:** [List Channel Users](https://pusher.com/docs/channels/library_auth_reference/rest-api/#get-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_name` | path | `string` | yes | The presence channel whose subscribed user IDs you want to fetch. |
