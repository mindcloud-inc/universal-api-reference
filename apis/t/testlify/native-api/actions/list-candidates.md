# List Candidates with Testlify

Retrieves candidates from Testlify with optional filters and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/candidate`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Candidates](https://docs.testlify.com/reference/get_candidate_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search query string. |
| `assessmentId` | query | `string` | no | Assessment identifier. |
| `email` | query | `string` | no | Filter by candidate email. |
| `candidateStatus` | query | `string` | no | Filter by candidate status. |
| `colName` | query | `string` | no | Column name to sort by. |
| `inOrder` | query | `string` | no | Sort order. |
| `limit` | query | `number` | no | Number of items to return. |
| `skip` | query | `number` | no | Number of items to skip. |
