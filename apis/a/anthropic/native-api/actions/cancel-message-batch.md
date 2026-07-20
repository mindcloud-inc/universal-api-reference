# Cancel Message Batch with Anthropic

Cancels a message batch in Anthropic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/batches/:message_batch_id/cancel`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Cancel Message Batch](https://platform.claude.com/docs/en/api/messages/batches/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_batch_id` | path | `string` | yes | The Message Batch ID. |
