# List Documents with Rossum

Retrieves documents from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Documents](https://rossum.app/api/docs/openapi/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `number` | no | Filter documents by Rossum email ID. |
| `page_size` | query | `number` | no | Number of documents to return (max 100). |
