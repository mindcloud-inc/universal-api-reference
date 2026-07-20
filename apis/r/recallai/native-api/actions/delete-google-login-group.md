# Delete Google Login Group with Recallai

Deletes a Google login group from Recallai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/google-login-groups/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Delete Google Login Group](https://docs.recall.ai/reference/google_login_groups_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this google login group. |
