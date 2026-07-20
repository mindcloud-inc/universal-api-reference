# Update email and password configuration with Neon

Updates email and password configuration in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/email_and_password`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update email and password configuration](https://api-docs.neon.tech/reference/updateneonauthemailandpasswordconfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `enabled` | body | `boolean` | no | Neon API parameter enabled |
| `email_verification_method` | body | `list` | no | Neon API parameter email_verification_method Accepted values: `0`, `1`. |
| `require_email_verification` | body | `boolean` | no | Neon API parameter require_email_verification |
| `auto_sign_in_after_verification` | body | `boolean` | no | Neon API parameter auto_sign_in_after_verification |
| `send_verification_email_on_sign_up` | body | `boolean` | no | Neon API parameter send_verification_email_on_sign_up |
| `send_verification_email_on_sign_in` | body | `boolean` | no | Neon API parameter send_verification_email_on_sign_in |
| `disable_sign_up` | body | `boolean` | no | Neon API parameter disable_sign_up |
