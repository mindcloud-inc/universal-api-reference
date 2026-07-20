# List Message Status History with TimelinesAI

Retrieves status history for a TimelinesAI message.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/{message_uid}/status_history`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [List Message Status History](https://timelinesai.mintlify.app/public-api-reference/get-the-sending-history-of-a-message-specified-by-the-messages-uid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_uid` | path | `string` | yes | UID of the message in the TimelinesAI workspace. |
