# Publish Log Event with LogSnag

## Endpoint

- **Method:** `POST`
- **Path:** `/log`
- **Base URL:** `https://api.logsnag.com/v1`
- **Official documentation:** [Publish Log Event](https://docs.logsnag.com/api-reference/log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name in LogSnag. |
| `channel` | body | `string` | yes | Channel name in LogSnag. |
| `event` | body | `string` | yes | Event title to publish. |
| `description` | body | `string` | no | Optional event description. |
| `icon` | body | `string` | no | Single emoji or emoji shortcode. |
| `notify` | body | `boolean` | no | Send a push notification for the event. |
| `parser` | body | `string` | no | Parse the description as markdown or plain text. |
| `tags` | body | `object` | no | Event tags as key/value pairs. |
| `timestamp` | body | `number` | no | Unix timestamp in seconds for historical data. |
| `user_id` | body | `string` | no | Associate the event with a user ID. |
