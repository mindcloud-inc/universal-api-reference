# Update Agent with Usedesk

Updates an existing agent in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/update/user`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Update Agent](https://api.usedocs.com/article/51416)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | body | `string` | no | Default group ID. |
| `name` | body | `string` | no | Agent name. |
| `role` | body | `string` | no | Agent role: admin, employee, or support. |
| `user_id` | body | `number` | yes | Agent ID. |
