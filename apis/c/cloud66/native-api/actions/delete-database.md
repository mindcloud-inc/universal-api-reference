# Delete Database with Cloud 66

Deletes a database from your Cloud 66 account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/stacks/:stack_id/server_groups/:server_group_id/databases/:id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Delete Database](https://developers.cloud66.com/v3/endpoints/databases/#delete-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Stack ID |
| `server_group_id` | path | `string` | yes | Server group ID |
| `id` | path | `string` | yes | Database UID |
