# Transfer Neon-managed auth project to your own account with Neon

Transfers Neon-managed auth project to your own account in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/auth/transfer_ownership`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Transfer Neon-managed auth project to your own account](https://api-docs.neon.tech/reference/transferneonauthproviderproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Neon API parameter project_id |
| `auth_provider` | body | `list` | yes | Neon API parameter auth_provider Accepted values: `0`, `1`, `2`, `3`. |
