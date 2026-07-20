# Send Bounce Notification with Sendcrux

Creates a bounce notification event in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notification`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Send Bounce Notification](https://api.sendbound.com/notification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bounce_type` | body | `string` | yes | The bounce subtype to report, such as hard. |
| `description` | body | `string` | no | A human-readable explanation for the bounce event. |
| `message_id` | body | `string` | yes | The provider message identifier associated with the bounce event. |
