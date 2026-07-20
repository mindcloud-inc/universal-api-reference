# Trigger Event with Pusher

Triggers an event in Pusher.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/{appId}/events`
- **Base URL:** `https://api-{cluster}.pusher.com`
- **Official documentation:** [Trigger Event](https://pusher.com/docs/channels/library_auth_reference/rest-api/#post-event-trigger-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `string` | no | Publish to a single channel. Use this instead of Channels when sending to one channel. |
| `channels[]` | body | `array<string>` | no | Publish to one or more channels. Pusher limits this array to 100 channels. |
| `data` | body | `string` | yes | The event payload. Pusher expects this as the event data value and limits it to 10KB. |
| `info` | body | `string` | no | Comma-separated channel attributes to return, such as user_count or subscription_count. |
| `name` | body | `string` | yes | The event name to publish. |
| `socket_id` | body | `string` | no | Exclude the event from being sent to a specific connection. |
