# Send Contact Event by Email with Dynosend

Creates an event in Dynosend for an email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Send Contact Event by Email](https://developers.dynosend.com/#sendanevent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `email` | body | `string` | yes | The email address of the contact the event belongs to. |
| `event_name` | body | `string` | yes | The event name to send. Use only letters, numbers, and underscores. |
