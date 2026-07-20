# Create Database with Cloud 66

Creates a database in your Cloud 66 account.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/server_groups/:server_group_id/databases`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Create Database](https://developers.cloud66.com/v3/endpoints/databases/#create-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Stack ID |
| `server_group_id` | path | `string` | yes | Server group ID |
| `database_name` | body | `string` | yes | Name for the new database |
| `database_user_ids[]` | body | `array<string>` | no | Database user UIDs to grant access to |
