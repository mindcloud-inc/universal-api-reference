# Get Server with Cloud 66

Retrieves a server from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/servers/:server_id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Get Server](https://developers.cloud66.com/v3/endpoints/servers/#get-server)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `server_id` | path | `string` | yes | The server UID |
