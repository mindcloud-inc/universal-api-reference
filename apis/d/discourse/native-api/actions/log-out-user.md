# Log Out User with Discourse

Logs an existing Discourse user out.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/users/:id/log_out.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Log Out User](https://docs.discourse.org/#tag/Users/operation/logOutUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User id. |
