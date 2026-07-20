# Regenerate Database User Password with Cloud 66

Regenerates a database user password in Cloud 66.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/server_groups/:server_group_id/database_users/:id/regenerate_password`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Regenerate Database User Password](https://developers.cloud66.com/v3/endpoints/database-users/#regenerate-database-user-password)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Stack ID |
| `server_group_id` | path | `string` | yes | Server group ID |
| `id` | path | `string` | yes | Database user UID |
