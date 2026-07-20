# Download Comment Attachment with Filestage

Downloads a Filestage comment attachment.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/{commentId}/attachments/{attachmentId}/contents`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Download Comment Attachment](https://developers.filestage.io/docs/api/ymynmgcr9km61-download-comment-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | yes | Comment Id |
| `attachmentId` | path | `string` | yes | Attachment Id |
