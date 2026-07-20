# List Databases with Cloud 66

Retrieves databases from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/server_groups/:server_group_id/databases`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [List Databases](https://developers.cloud66.com/v3/endpoints/databases/#list-databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Stack ID |
| `server_group_id` | path | `string` | yes | Server group ID |
