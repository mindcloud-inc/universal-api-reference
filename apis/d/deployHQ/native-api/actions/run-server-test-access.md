# Run Server Test Access with DeployHQ

Runs a server access test in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/servers/:server_id/test_access`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Run Server Test Access](https://api.deployhq.com/docs#tag/Test-Access/operation/createProjectServerTestAccess)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `server_id` | path | `string` | yes | ID of the server to test. |
