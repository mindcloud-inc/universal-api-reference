# Get Google Login with Recallai

Retrieves a Google login from Recallai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/google-logins/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Get Google Login](https://docs.recall.ai/reference/google_logins_retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | A UUID string identifying this google login. |
