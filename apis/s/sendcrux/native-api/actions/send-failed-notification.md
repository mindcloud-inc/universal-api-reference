# Send Failed Notification with Sendcrux

Creates a failed notification event in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notification`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Send Failed Notification](https://api.sendbound.com/notification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | A human-readable explanation for the failed event. |
| `message_id` | body | `string` | yes | The provider message identifier associated with the failed event. |
