# Retrieve Download Content with Rossum

Retrieves a document download archive from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/downloads/:documentsDownloadID/content`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Retrieve Download Content](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentsDownloadID` | path | `number` | yes | ID of the Rossum download whose archive content should be retrieved. |
