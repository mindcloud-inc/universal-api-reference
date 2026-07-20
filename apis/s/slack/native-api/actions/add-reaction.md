# Add Reaction with Slack

Adds a reaction to an item in Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `reactions.add`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Add Reaction](https://docs.slack.dev/reference/methods/reactions.add/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list<string>` | yes | Channel where the message to add reaction to was posted. |
| `timestamp` | body | `list<string>` | yes | Timestamp of the message to add reaction to. |
| `name` | body | `string` | yes | Reaction (emoji) name. Ex: thumbsup |
| `senderOverride` | body | `list` | no | Override the connection's Default Sender for this action only. Accepted values: `bot`, `user`. Format: `toggle`. |
