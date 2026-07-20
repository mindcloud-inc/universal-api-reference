# Add Group Members with Discourse

Adds members to a Discourse group.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:id/members.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Add Group Members](https://docs.discourse.org/#tag/Groups/operation/addGroupMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Group id. |
| `usernames` | body | `string` | yes | Comma-separated usernames to add. |
