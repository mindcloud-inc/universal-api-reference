# Invite To Topic with Discourse

Invites a user to a Discourse topic.

## Endpoint

- **Method:** `POST`
- **Path:** `/t/:id/invite.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Invite To Topic](https://docs.discourse.org/#tag/Topics/operation/inviteToTopic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address to invite to the topic. |
| `id` | path | `number` | yes | Topic id. |
| `user` | body | `string` | no | Username to invite to the topic. |
