# Get email and password configuration with Neon

Retrieves email and password configuration from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/email_and_password`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get email and password configuration](https://api-docs.neon.tech/reference/getneonauthemailandpasswordconfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
