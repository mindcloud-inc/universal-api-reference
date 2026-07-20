# List Channel Members with Slack

Retrieves conversation members from a Slack workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `conversations.members`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Channel Members](https://docs.slack.dev/reference/methods/conversations.members/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `list<string>` | yes | ID of the conversation to retrieve members for. |
| `sendAsBot` | query | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
