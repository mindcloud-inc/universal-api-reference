# Get Channel Information with Slack

Retrieves conversation details from a Slack workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `conversations.info`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Get Channel Information](https://docs.slack.dev/reference/methods/conversations.info/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `list<string>` | yes | Conversation ID to learn more about |
| `include_locale` | query | `boolean` | no | Set this to true to receive the locale for this conversation. Format: `toggle`. |
| `include_num_members` | query | `boolean` | no | Set to true to include the member count for the specified conversation. Format: `toggle`. |
