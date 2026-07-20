# Set Channel Topic with Slack

Updates a conversation topic in Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations.setTopic`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Set Channel Topic](https://docs.slack.dev/reference/methods/conversations.setTopic/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | yes | Conversation to set the topic of. |
| `topic` | body | `string` | yes | The new topic string. Does not support formatting or linkification. |
| `sendAsBot` | body | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
