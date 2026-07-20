# Create Lead Comment with noCRM.io

Creates a new lead comment in noCRM.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:lead_id/comments`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Create Lead Comment](https://www.nocrm.io/api#create-a-comment-on-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Lead ID. |
| `content` | body | `string` | yes | Comment content. |
| `user_id` | body | `string` | no | User email or ID for comment ownership. |
| `attachments` | body | `list<object>` | no | Attachments to add on the comment. |
| `activity_id` | body | `number` | no | Activity ID to set on the comment. |
| `created_at` | body | `date` | no | Override comment creation date. |
