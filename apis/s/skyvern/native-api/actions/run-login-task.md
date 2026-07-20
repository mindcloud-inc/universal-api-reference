# Run Login Task with Skyvern

Runs a login automation task in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/run/tasks/login`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Run Login Task](https://www.skyvern.com/docs/api-reference/agent/login-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credential_id` | body | `string` | no | ID of the Skyvern credential to use for login |
| `credential_type` | body | `string` | yes | Credential provider to use for the login flow. |
| `url` | body | `string` | no | Website URL for the login task. |
