# Update Lead Comment with noCRM.io

Updates an existing lead comment in noCRM.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/:lead_id/comments/:id`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Update Lead Comment](https://www.nocrm.io/api#update-a-comment-on-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Lead ID. |
| `id` | path | `string` | yes | Comment ID. |
| `content` | body | `string` | yes | Replacement comment content. |
| `activity_id` | body | `number` | no | Activity ID to set on the comment. |
| `is_pinned` | body | `boolean` | no | Whether the comment is pinned. |
