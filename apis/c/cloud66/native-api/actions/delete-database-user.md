# Delete Database User with Cloud 66

Deletes a database user from your Cloud 66 account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/stacks/:stack_id/server_groups/:server_group_id/database_users/:id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Delete Database User](https://developers.cloud66.com/v3/endpoints/database-users/#delete-database-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Stack ID |
| `server_group_id` | path | `string` | yes | Server group ID |
| `id` | path | `string` | yes | Database user UID |
