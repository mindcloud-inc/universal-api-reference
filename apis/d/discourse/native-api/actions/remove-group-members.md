# Remove Group Members with Discourse

Removes members from a Discourse group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:id/members.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Remove Group Members](https://docs.discourse.org/#tag/Groups/operation/removeGroupMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Group id. |
| `usernames` | body | `string` | yes | Comma-separated usernames to remove. |
