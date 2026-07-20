# Upload Project Document with CompanyCam

Upload a document to a CompanyCam project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:projectId/documents`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Upload Project Document](https://docs.companycam.com/reference/listprojectdocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document.name` | body | `string` | no | — |
| `projectId` | path | `string` | yes | — |
| `document` | body | `object` | no | — |
| `document.attachment` | body | `file` | no | Base64 encoded file contents with 30 MB limit |
