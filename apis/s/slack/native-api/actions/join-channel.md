# Join Channel with Slack

Joins an existing conversation in Slack.

## Endpoint

- **Method:** `GET`
- **Path:** `conversations.join`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Join Channel](https://docs.slack.dev/reference/methods/conversations.join/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `list<string>` | yes | ID of conversation to join |
| `sendAsBot` | query | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
