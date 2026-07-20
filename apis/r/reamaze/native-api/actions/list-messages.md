# List Messages with Reamaze

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [List Messages](https://www.reamaze.com/api/get_messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | `filter` with `staff` will show only staff messages and `customer` will show only customer messages. |
| `staff` | query | `string` | no | `filter` with `staff` will show only staff messages and `customer` will show only customer messages. |
| `tag` | query | `string` | no | `tag` with string value (comma separated) will return messages belonging to conversations matching specific tags. |
| `origin` | query | `string` | no | `origin` with number value will return messages from a specific origin (see below note on origin values). |
| `sent_by` | query | `string` | no | `sent_by` with a value matching a known user `email` will return only messages sent by that user. |
| `email` | query | `string` | no | `sent_by` with a value matching a known user `email` will return only messages sent by that user. |
| `category` | query | `string` | no | `category` with a string value will return messages from a specific Channel (internally called `category`) matching the `slug` value. |
| `start_date` | query | `date` | no | `start_date` and `end_date` (ISO8601 format) will allow filtering of messages by creation date. |
| `end_date` | query | `date` | no | `start_date` and `end_date` (ISO8601 format) will allow filtering of messages by creation date. |
| `include` | query | `string` | no | `include` with the value `original_body` will return an additional `original_body` attribute that is the message's HTML, if present. |
| `original_body` | query | `string` | no | `include` with the value `original_body` will return an additional `original_body` attribute that is the message's HTML, if present. |
