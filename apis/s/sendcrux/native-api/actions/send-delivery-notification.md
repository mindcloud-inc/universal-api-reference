# Send Delivery Notification with Sendcrux

Creates a delivery notification event in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notification`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Send Delivery Notification](https://api.sendbound.com/notification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | body | `string` | yes | The provider message identifier associated with the sent event. |
