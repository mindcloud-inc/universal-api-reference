# Reply to a comment with ConnectSafely

Post a reply to an existing comment on a LinkedIn post. Replies appear threaded under the original comment. Optionally tag a member with a real @mention that notifies them (e.g. the original commenter) by passing `mention`. Useful for continuing conversations and engaging with community discussions.

## Endpoint

- **Method:** `POST`
- **Path:** `/reply`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Reply to a comment](https://connectsafely.ai/docs/api/linkedin-posts/post-reply-reply-to-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `commentId` | body | `string` | yes | ID of the comment to reply to (from /posts/comments response) |
| `reply` | body | `string` | yes | Reply text content. Supports hashtags. When `mention` is provided, place a {{user}} placeholder where the tag should appear — otherwise the tagged member's name is prepended. |
| `mention` | body | `object` | no | Optional @mention to tag a member in the reply. Produces a real LinkedIn tag that notifies the member (e.g. tag the original commenter). The visible tag replaces the {{user}} placeholder in `reply` (or is prepended if no placeholder is present). |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `replyId` | `string` |  |
