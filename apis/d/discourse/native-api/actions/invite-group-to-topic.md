# Invite Group To Topic with Discourse

Invites a group to a Discourse topic.

## Endpoint

- **Method:** `POST`
- **Path:** `/t/:id/invite-group.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Invite Group To Topic](https://docs.discourse.org/#tag/Topics/operation/inviteGroupToTopic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | body | `string` | yes | Group name to invite to the topic. |
| `id` | path | `number` | yes | Topic id. |
| `should_notify` | body | `boolean` | no | Whether to notify the group. |
