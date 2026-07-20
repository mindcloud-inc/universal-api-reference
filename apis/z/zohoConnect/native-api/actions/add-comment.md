# Add Comment with Zoho Connect

Creates a new comment in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/v2/addComment`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Add Comment](https://www.zoho.com/connect/api/add-comment.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | ID of the network where the comment should be added. |
| `streamId` | query | `string` | yes | The post to comment on. |
| `parentCommentId` | query | `string` | no | Reply to an existing comment by supplying its comment ID. |
| `commentContent` | query | `string` | yes | Comment text. Maximum length is 10000 characters and it supports mentions plus rich formatting. |
| `fileIds` | query | `string` | no | Comma-separated file IDs from the upload Files API. Up to 10 files can be attached. Send multiple values as a string separated by `,`. |
