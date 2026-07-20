# List User Reactions with Slack

Retrieves reactions made by a Slack user.

## Endpoint

- **Method:** `GET`
- **Path:** `reactions.list`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List User Reactions](https://docs.slack.dev/reference/methods/reactions.list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `list` | yes | Show reactions made by this user. Defaults to the authed user. |
| `full` | query | `boolean` | no | If true always return the complete reaction list. Format: `toggle`. |
