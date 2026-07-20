# Kick User From Channel with Slack

Removes a user from a Slack conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations.kick`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Kick User From Channel](https://docs.slack.dev/reference/methods/conversations.kick/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | yes | ID of conversation to remove user from. |
| `user` | body | `list` | yes | User ID to be removed. |
| `sendAsBot` | body | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
