# Download Document with Incontrol

Downloads a document from Incontrol in the requested file type.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/document/{{id}}/download`
- **Base URL:** `https://portal.incontrol.app`
- **Official documentation:** [Download Document](https://portal.incontrol.app/swagger/index.html?urls.primaryName=Public%20API%20(v1))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The document ID. |
| `fileType` | query | `string` | no | The type of file that should be returned. |
