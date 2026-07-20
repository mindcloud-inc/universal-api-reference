# Update email provider configuration with Neon

Updates email provider configuration in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/email_provider`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update email provider configuration](https://api-docs.neon.tech/reference/updateneonauthemailprovider)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `requestBody` | body | `object` | yes | Neon API parameter requestBody |
