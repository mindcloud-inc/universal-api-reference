# Retrieve Document Content with Rossum

Retrieves original document content from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentID/content`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Retrieve Document Content](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentID` | path | `number` | yes | ID of the document whose file content should be retrieved. |
