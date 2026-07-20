# Send Message with Timetonic

Creates a new message in Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Send Message](https://timetonic.com/live/api.php?doc=#sendMsg-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msg` | body | `string` | yes | Message text to send. |
| `b_c` | body | `string` | no | Optional code of the book that will receive the message. |
| `b_o` | body | `string` | no | Optional owner of the book that will receive the message. |
| `msg_id` | body | `string` | no | Optional message id when editing an existing message. |
| `body` | body | `string` | no | Optional message body payload. |
| `event` | body | `string` | no | Optional event value associated with the message. |
| `uid` | body | `string` | no | Optional client UUID for the message. |
