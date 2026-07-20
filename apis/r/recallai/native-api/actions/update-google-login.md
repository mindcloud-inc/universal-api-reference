# Update Google Login with Recallai

Updates an existing Google login in Recallai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/google-logins/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Update Google Login](https://docs.recall.ai/reference/google_logins_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The email address of the google account to use for login. |
| `group_id` | body | `string` | no | The id of the login group this login belongs to. |
| `id` | path | `string` | yes | A UUID string identifying this google login. |
| `is_active` | body | `boolean` | no | If the login should be used for round robin. (default: true) |
| `sso_v2_cert` | body | `string` | no | PEM-formatted x509 certificate which is registered in your Google Workspace SSO Profile. |
| `sso_v2_private_key` | body | `string` | no | PEM-formatted private key used for signing SSO requests. |
| `sso_v2_workspace_domain` | body | `string` | no | The primary domain name of your Google Workspace Account used for SSO. |
