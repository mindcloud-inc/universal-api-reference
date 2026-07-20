# Get Message Reactions with TimelinesAI

Retrieves reactions for a TimelinesAI message.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/{message_uid}/reactions`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Get Message Reactions](https://timelinesai.mintlify.app/public-api-reference/get-the-current-reactions-map-for-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_uid` | path | `string` | yes | UID of the message in the TimelinesAI workspace. |
