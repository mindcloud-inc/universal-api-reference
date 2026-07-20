# Create File Upload URL with Agentset

Creates a presigned file upload URL in Agentset.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/uploads`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Create File Upload URL](https://docs.agentset.ai/api-reference/endpoint/uploads/single)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentType` | body | `string` | yes | The MIME type of the file. |
| `fileName` | body | `string` | yes | The file name for the presigned upload URL. |
| `fileSize` | body | `number` | yes | The file size in bytes. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
