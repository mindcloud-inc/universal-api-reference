# Create Agent with Usedesk

Creates a new agent in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/create/user`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Create Agent](https://api.usedocs.com/article/51415)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Agent name. |
| `role` | body | `string` | no | Agent role: admin, employee, or support. |
| `email` | body | `string` | yes | Agent email. |
| `password` | body | `string` | yes | Agent password. |
| `group` | body | `number` | yes | Default group ID. |
