# Retrieve Message Batch Results with Anthropic

Retrieves results for an Anthropic message batch.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages/batches/:message_batch_id/results`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Retrieve Message Batch Results](https://platform.claude.com/docs/en/api/messages/batches/results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_batch_id` | path | `string` | yes | The Message Batch ID. |
