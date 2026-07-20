# Get SSH Credentials with Cloud CLI

Retrieves SSH credentials for a Cloud CLI environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments/:id/credentials`
- **Base URL:** `https://cloudcli.ai/api/v1`
- **Official documentation:** [Get SSH Credentials](https://developer.cloudcli.ai/get-ssh-credentials-3998773e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Environment ID. |
