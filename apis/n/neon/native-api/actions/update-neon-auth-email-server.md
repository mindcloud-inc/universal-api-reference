# Update email server configuration with Neon

Updates email server configuration in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/auth/email_server`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update email server configuration](https://api-docs.neon.tech/reference/updateneonauthemailserver)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `requestBody` | body | `object` | yes | Neon API parameter requestBody |
