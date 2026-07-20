# Delete Issue Comment with Supabugs

Deletes a comment from a Supabugs issue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/issues/:issueId/comments/:id`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [Delete Issue Comment](https://api.supabugs.io/api/public/v1/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueId` | path | `string` | yes | Supabugs issue id. |
| `id` | path | `string` | yes | Supabugs comment id. |
