# Create Group with Discourse

Creates a new group in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/groups.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Group](https://docs.discourse.org/#tag/Groups/operation/createGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group.name` | body | `string` | yes | Group name. |
| `group.full_name` | body | `string` | no | Optional group display name. |
