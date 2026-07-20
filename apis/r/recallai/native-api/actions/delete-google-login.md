# Delete Google Login with Recallai

Deletes an existing Google login from Recallai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/google-logins/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Delete Google Login](https://docs.recall.ai/reference/google_logins_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this google login. |
