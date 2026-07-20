# List Group Members with Discourse

Retrieves members of a Discourse group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:name/members.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List Group Members](https://docs.discourse.org/#tag/Groups/operation/listGroupMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Discourse group name. |
