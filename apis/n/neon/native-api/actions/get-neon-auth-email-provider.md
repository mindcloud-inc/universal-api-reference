# Get email provider configuration with Neon

Retrieves email provider configuration from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/email_provider`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get email provider configuration](https://api-docs.neon.tech/reference/getneonauthemailprovider)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
