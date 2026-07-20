# Set Presence with Slack

Updates the current user's Slack presence.

## Endpoint

- **Method:** `POST`
- **Path:** `users.setPresence`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Set Presence](https://docs.slack.dev/reference/methods/users.setPresence/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presence` | body | `list` | no | Value should be one of auto or away |
| `sendAsBot` | body | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
