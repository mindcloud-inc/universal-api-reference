# Send Flow Message with Marketing Master IO

Sends a flow message to a subscriber in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messenger/sending/:subscriber_id/messages/:payload_id`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Send Flow Message](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_tag` | body | `string` | no | Optional Facebook message tag for the outbound send. |
| `payload_id` | path | `string` | yes | — |
| `subscriber_id` | path | `string` | yes | — |
