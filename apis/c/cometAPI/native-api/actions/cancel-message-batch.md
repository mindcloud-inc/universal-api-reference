# Cancel Message Batch with CometAPI

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/batches/:message_batch_id/cancel`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Cancel Message Batch](https://www.cometapi.com/claude-opus-4-5-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_batch_id` | path | `string` | yes | Message batch ID to cancel. |
