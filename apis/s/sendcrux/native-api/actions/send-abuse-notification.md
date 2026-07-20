# Send Abuse Notification with Sendcrux

Creates an abuse notification event in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notification`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Send Abuse Notification](https://api.sendbound.com/notification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | A human-readable explanation for the abuse event. |
| `message_id` | body | `string` | yes | The provider message identifier associated with the abuse event. |
| `report_type` | body | `string` | yes | The abuse report type, such as hard. |
