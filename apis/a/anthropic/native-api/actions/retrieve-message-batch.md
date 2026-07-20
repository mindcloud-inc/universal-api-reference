# Retrieve Message Batch with Anthropic

Retrieves a message batch from Anthropic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages/batches/:message_batch_id`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Retrieve Message Batch](https://platform.claude.com/docs/en/api/messages/batches/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_batch_id` | path | `string` | yes | The Message Batch ID. |
