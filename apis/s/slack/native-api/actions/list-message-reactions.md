# List Message Reactions with Slack

Retrieves reactions for an item in Slack.

## Endpoint

- **Method:** `GET`
- **Path:** `reactions.get`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Message Reactions](https://docs.slack.dev/reference/methods/reactions.get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `list<string>` | yes | Channel where the message to get reactions for was posted. |
| `timestamp` | query | `list<string>` | yes | Timestamp of the message to get reactions for. |
| `full` | query | `boolean` | no | If true always return the complete reaction list. Format: `toggle`. |
