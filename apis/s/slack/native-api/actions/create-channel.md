# Create Channel with Slack

Creates a new channel in Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations.create`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Create Channel](https://docs.slack.dev/reference/methods/conversations.create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the public or private channel to create |
| `is_private` | body | `boolean` | no | Create a private channel instead of a public one Format: `toggle`. |
| `sendAsBot` | body | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
