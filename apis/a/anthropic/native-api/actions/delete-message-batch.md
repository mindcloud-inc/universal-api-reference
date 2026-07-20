# Delete Message Batch with Anthropic

Deletes a message batch from Anthropic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/messages/batches/:message_batch_id`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Delete Message Batch](https://platform.claude.com/docs/en/api/messages/batches/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_batch_id` | path | `string` | yes | The Message Batch ID. |
