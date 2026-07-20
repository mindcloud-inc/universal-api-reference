# List Channels with Slack

Retrieves channels from a Slack workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `conversations.list`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Channels](https://docs.slack.dev/reference/methods/conversations.list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `types` | query | `list<string>` | no | Send multiple values as a array. |
| `exclude_archived` | query | `boolean` | no | Format: `toggle`. |
| `sendAsBot` | query | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
