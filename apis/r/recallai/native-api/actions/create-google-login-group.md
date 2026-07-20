# Create Google Login Group with Recallai

Creates a new Google login group in Recallai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/google-login-groups/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Create Google Login Group](https://docs.recall.ai/reference/google_login_groups_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login_mode` | body | `string` | yes | * `always` - Always * `only_if_required` - Only If Required |
| `name` | body | `string` | yes | Name of the login group. It can used to filter out login groups when retrieving them via API. |
