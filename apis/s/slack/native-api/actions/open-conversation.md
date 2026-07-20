# Open Conversation with Slack

Opens or resumes a direct conversation in Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations.open`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Open Conversation](https://docs.slack.dev/reference/methods/conversations.open/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `users` | body | `list<string>` | yes | Comma separated lists of users. If only one user is included, this creates a 1:1 DM. The ordering of the users is preserved whenever a multi-person direct message is returned. Supply a channel when not supplying users. Send multiple values as a string. |
| `channel` | body | `list<string>` | no | Resume a conversation by supplying an im or mpim's ID. Or provide the users field instead. |
| `prevent_creation` | body | `boolean` | no | Do not create a direct message or multi-person direct message. This is used to see if there is an existing dm or mpdm. Format: `toggle`. |
| `return_im` | body | `boolean` | no | Indicates you want the full conversation object in the response. Format: `toggle`. |
