# Deactivate User with Discourse

Deactivates an existing user in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/users/:id/deactivate.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Deactivate User](https://docs.discourse.org/#tag/Users/operation/deactivateUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User id. |
| `confirm` | body | `boolean` | no | Optional confirmation flag for deactivation. |
