# Update Message Reactions with TimelinesAI

Updates reactions on an existing TimelinesAI message.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messages/{message_uid}/reactions`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Update Message Reactions](https://timelinesai.mintlify.app/public-api-reference/update-reactions-for-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_uid` | path | `string` | yes | UID of the message in the TimelinesAI workspace. |
| `reaction` | body | `string` | yes | Reaction emoji to set for the message. |
