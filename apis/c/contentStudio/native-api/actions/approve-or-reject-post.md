# Approve or Reject Post with ContentStudio

Approves or rejects a post under review in ContentStudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspace_id/posts/:post_id/approval`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [Approve or Reject Post](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Approval action to perform. |
| `comment` | body | `string` | no | Optional approval comment. |
| `post_id` | path | `string` | yes | ContentStudio post ID. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
