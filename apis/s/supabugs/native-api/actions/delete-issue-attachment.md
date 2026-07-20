# Delete Issue Attachment with Supabugs

Deletes an attachment from a Supabugs issue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/issues/:issueId/attachments/:id`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [Delete Issue Attachment](https://api.supabugs.io/api/public/v1/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueId` | path | `string` | yes | Supabugs issue id. |
| `id` | path | `string` | yes | Supabugs attachment id. |
