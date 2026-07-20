# Stream Patient Document with Cerbo

Streams patient document content from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:document_id/stream`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Stream Patient Document](https://docs.cer.bo/#tag/Patient-Documents/operation/streamPatientDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `number` | no | ID of document |
