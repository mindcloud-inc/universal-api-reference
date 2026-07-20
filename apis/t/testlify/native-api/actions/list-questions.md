# List Questions with Testlify

Retrieves Testlify questions with optional filters and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/question`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Questions](https://docs.testlify.com/reference/get_questions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search query string. |
| `type` | query | `string` | no | Question type. |
| `difficulty` | query | `string` | no | Question difficulty. |
| `testLibraryId` | query | `string` | no | Filter by test library. |
| `isCompanyTestLibraries` | query | `boolean` | no | Include company test libraries. |
| `isTestlifyLibraries` | query | `boolean` | no | Include Testlify libraries. |
| `language` | query | `string` | no | Question language. |
| `isStarred` | query | `boolean` | no | Filter starred questions. |
| `isCompanyTest` | query | `boolean` | no | Include company test questions. |
| `limit` | query | `number` | no | Number of items to return. |
| `skip` | query | `number` | no | Number of items to skip. |
