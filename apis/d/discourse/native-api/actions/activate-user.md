# Activate User with Discourse

Activates an existing user in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/users/:id/activate.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Activate User](https://docs.discourse.org/#tag/Users/operation/activateUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User id. |
| `confirm` | body | `string` | no | Optional confirmation flag if required by the provider. |
