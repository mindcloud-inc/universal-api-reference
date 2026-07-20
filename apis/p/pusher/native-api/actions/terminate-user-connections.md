# Terminate User Connections with Pusher

Terminates a user's connections in Pusher.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/{appId}/users/:user_id/terminate_connections`
- **Base URL:** `https://api-{cluster}.pusher.com`
- **Official documentation:** [Terminate User Connections](https://pusher.com/docs/channels/library_auth_reference/rest-api/#post-terminate-user-connections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | The authenticated user whose active connections should be terminated. |
