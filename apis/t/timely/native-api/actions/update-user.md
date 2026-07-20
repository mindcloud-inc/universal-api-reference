# Update User with Timely

Updates an existing user in Timely.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.1/{account_id}/users/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Update User](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Workspace id |
| `id` | path | `number` | yes | User id |
| `user` | body | `object` | yes | — |
