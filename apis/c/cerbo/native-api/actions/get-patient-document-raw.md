# Get Patient Document Raw with Cerbo

Retrieves raw patient document content from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:document_id/content`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Document Raw](https://docs.cer.bo/#tag/Patient-Documents/operation/showPatientDocumentRaw)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `number` | no | ID of document |
