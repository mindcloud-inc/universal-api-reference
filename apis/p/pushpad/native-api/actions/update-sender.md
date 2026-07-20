# Update Sender with Pushpad

Updates an existing sender in Pushpad.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/senders/:sender_id`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Update Sender](https://pushpad.xyz/docs/rest_api#senders_api_docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `sender_id` | path | `number` | yes |
