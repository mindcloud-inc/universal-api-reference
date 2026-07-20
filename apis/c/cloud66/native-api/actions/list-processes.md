# List Processes with Cloud 66

Retrieves processes from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/processes`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [List Processes](https://developers.cloud66.com/v3/endpoints/processes/#list-processes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `server_uid` | query | `number` | no | Filter processes by server ID |
