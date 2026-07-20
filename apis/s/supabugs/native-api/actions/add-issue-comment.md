# Add Issue Comment with Supabugs

Creates a new comment on a Supabugs issue.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/:id/comments`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [Add Issue Comment](https://api.supabugs.io/api/public/v1/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Supabugs issue id. |
| `content` | body | `string` | yes | Comment text. |
