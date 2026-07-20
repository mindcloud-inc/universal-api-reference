# Update Google Login Group with Recallai

Updates a Google login group in Recallai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/google-login-groups/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Update Google Login Group](https://docs.recall.ai/reference/google_login_groups_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this google login group. |
| `login_mode` | body | `string` | no | * `always` - Always * `only_if_required` - Only If Required |
| `name` | body | `string` | no | Name of the login group. It can used to filter out login groups when retrieving them via API. |
