# Delete Message with Zulip

Deletes an existing message from Zulip.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/messages/:message_id`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Delete Message](https://zulip.com/api/delete-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `number` | yes | The target message ID. |
