# List Documents with Cradl AI

Retrieves all documents from Cradl AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [List Documents](https://docs.cradl.ai/api-reference/get-documents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | query | `string` | no | Dataset filter for documents. |
| `documentId` | query | `string` | no | Document ID filter. |
| `consentId` | query | `string` | no | Consent filter for documents. |
| `sortBy` | query | `string` | no | Field to sort documents by. |
| `order` | query | `string` | no | Sort order. |
