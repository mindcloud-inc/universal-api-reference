# Create Database User with Cloud 66

Creates a database user in your Cloud 66 account.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/server_groups/:server_group_id/database_users`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Create Database User](https://developers.cloud66.com/v3/endpoints/database-users/#create-database-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Stack ID |
| `server_group_id` | path | `string` | yes | Server group ID |
| `username` | body | `string` | yes | Database username to create |
| `database_ids[]` | body | `array<string>` | no | Database UIDs to grant access to |
| `user_type` | body | `string` | yes | Supported database user type |
