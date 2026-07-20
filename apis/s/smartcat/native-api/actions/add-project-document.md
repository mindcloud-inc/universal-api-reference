# Add Project Document with Smartcat

Adds a document to a Smartcat project.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/v1/project/document`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Add Project Document](https://developers.smartcat.com/api/#add-a-document-to-the-project)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `string` | yes | Target Smartcat project ID |
| `Request` | body | `string<object>` | yes | JSON array with one object per uploaded file, in the same order as the FILE parts. |
| `FILE_1` | body | `file` | yes | — |
| `FILE_2` | body | `file` | no | — |
