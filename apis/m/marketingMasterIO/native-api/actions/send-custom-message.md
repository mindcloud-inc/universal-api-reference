# Send Custom Message with Marketing Master IO

Sends a custom message to a subscriber in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messenger/sending/:subscriber_id/custom`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Send Custom Message](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `object` | yes | Custom message payload to send. |
| `message_tag` | body | `string` | no | Optional Facebook message tag for sends outside the standard window. |
| `subscriber_id` | path | `string` | yes | — |
