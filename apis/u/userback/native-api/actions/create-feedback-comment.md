# Create Feedback Comment with Userback

Creates a comment on a Userback feedback item.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback/comment`
- **Base URL:** `https://rest.userback.io/1.0`
- **Official documentation:** [Create Feedback Comment](https://docs.userback.io/reference/createfeedbackcomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedbackId` | body | `number` | yes | Parent feedback ID. |
| `comment` | body | `string` | yes | Feedback comment text. |
| `isPublic` | body | `boolean` | no | Whether the comment is public. |
| `replyCommentId` | body | `number` | no | Reply target comment ID. |
| `userId` | body | `number` | no | Comment author user ID. |
| `guestEmail` | body | `string` | no | Guest commenter email. |
| `guestName` | body | `string` | no | Guest commenter name. |
