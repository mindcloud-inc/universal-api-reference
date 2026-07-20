# List Database Users with Cloud 66

Retrieves database users from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/server_groups/:server_group_id/database_users`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [List Database Users](https://developers.cloud66.com/v3/endpoints/database-users/#list-database-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Stack ID |
| `server_group_id` | path | `string` | yes | Server group ID |
| `show_password` | query | `boolean` | no | Include password in the response when permitted |
