# Get Framework Document with Openlayer

Retrieves a framework document from Openlayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/frameworks/:frameworkId/documents/:documentId`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Get Framework Document](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Openlayer framework document ID. |
| `frameworkId` | path | `string` | yes | Openlayer framework ID. |
