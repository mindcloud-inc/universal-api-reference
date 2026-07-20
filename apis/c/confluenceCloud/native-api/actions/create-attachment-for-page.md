# Create Attachment For Page with Confluence

Creates a new attachment for a Confluence page.

## Endpoint

- **Method:** `POST`
- **Path:** `/ex/confluence/:cloudId/wiki/rest/api/content/:id/child/attachment`
- **Base URL:** `https://api.atlassian.com`
- **Official documentation:** [Create Attachment For Page](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content---attachments/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloudId` | path | `string` | yes | Confluence cloud ID for the target site. |
| `id` | path | `string` | yes | Confluence page ID to attach the file to. |
| `file` | body | `file` | yes | File content to upload as the attachment. |
| `comment` | body | `string` | no | Optional attachment comment. |
| `minorEdit` | body | `boolean` | no | Whether the upload should be marked as a minor edit. |
