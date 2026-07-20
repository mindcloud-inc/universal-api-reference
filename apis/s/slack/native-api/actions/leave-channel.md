# Leave Channel with Slack

Leaves an existing conversation in Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations.leave`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Leave Channel](https://docs.slack.dev/reference/methods/conversations.leave/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list<string>` | yes | Conversation to leave |
| `sendAsBot` | body | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
