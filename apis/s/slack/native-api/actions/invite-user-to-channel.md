# Invite User to Channel with Slack

Invites users to a Slack channel.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations.invite`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Invite User to Channel](https://docs.slack.dev/reference/methods/conversations.invite/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list<string>` | yes | The ID of the public or private channel to invite user(s) to. |
| `users` | body | `list` | yes | A comma separated list of user IDs. Up to 1000 users may be listed. Send multiple values as a array. |
| `sendAsBot` | body | `boolean` | no | Determines if this action should be performed by the current user or the Mindcloud bot. Format: `toggle`. |
| `force` | body | `boolean` | no | When set to true and multiple user IDs are provided, continue inviting the valid ones while disregarding invalid IDs. Format: `toggle`. |
