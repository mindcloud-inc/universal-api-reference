# Send Spam Notification with Sendcrux

Creates a spam notification event in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notification`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Send Spam Notification](https://api.sendbound.com/notification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | A human-readable explanation for the spam event. |
| `message_id` | body | `string` | yes | The provider message identifier associated with the spam event. |
| `report_type` | body | `string` | yes | The spam report type, such as hard. |
