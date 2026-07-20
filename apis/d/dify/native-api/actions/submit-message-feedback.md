# Submit Message Feedback with Dify

Creates message feedback in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/:message_id/feedbacks`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Submit Message Feedback](https://docs.dify.ai/api-reference/feedback/submit-message-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | Message ID to attach feedback to. |
| `rating` | body | `string` | no | Feedback rating: like, dislike, or null to revoke. |
| `user` | body | `string` | yes | User identifier. |
| `content` | body | `string` | no | Optional text feedback content. |
