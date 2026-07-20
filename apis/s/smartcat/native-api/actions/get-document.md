# Get Document with Smartcat

Retrieves document details from the Smartcat account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/v1/document`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Get Document](https://developers.smartcat.com/api/#fetch-the-document-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | query | `string` | yes | Document ID in the format documentId_targetLanguageId |
