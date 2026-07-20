# Update organization plugin configuration with Neon

Updates organization plugin configuration in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/plugins/organization`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update organization plugin configuration](https://api-docs.neon.tech/reference/updateneonauthorganizationplugin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `enabled` | body | `boolean` | no | Neon API parameter enabled |
| `organization_limit` | body | `number` | no | Neon API parameter organization_limit |
| `membership_limit` | body | `number` | no | Neon API parameter membership_limit |
| `creator_role` | body | `list` | no | Neon API parameter creator_role Accepted values: `0`, `1`. |
| `send_invitation_email` | body | `boolean` | no | Neon API parameter send_invitation_email |
