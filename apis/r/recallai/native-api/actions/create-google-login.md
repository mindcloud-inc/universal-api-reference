# Create Google Login with Recallai

Creates a new Google login in Recallai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/google-logins/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Create Google Login](https://docs.recall.ai/reference/google_logins_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the google account to use for login. |
| `group_id` | body | `string` | yes | The id of the login group this login belongs to. |
| `is_active` | body | `boolean` | no | If the login should be used for round robin. (default: true) |
| `sso_v2_cert` | body | `string` | yes | PEM-formatted x509 certificate which is registered in your Google Workspace SSO Profile. |
| `sso_v2_private_key` | body | `string` | yes | PEM-formatted private key used for signing SSO requests. |
| `sso_v2_workspace_domain` | body | `string` | yes | The primary domain name of your Google Workspace Account used for SSO. |
