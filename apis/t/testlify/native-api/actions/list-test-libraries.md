# List Test Libraries with Testlify

Retrieves Testlify test libraries with optional filters and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/test/library/search`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Test Libraries](https://docs.testlify.com/reference/get_test_libraries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search query string. |
| `type` | query | `string` | no | Test library type. |
| `difficulty` | query | `string` | no | Test difficulty. |
| `jobRoleId` | query | `string` | no | Job role identifier. |
| `isCompanyTest` | query | `boolean` | no | Include company tests. |
| `isTestlifyLibraries` | query | `boolean` | no | Include Testlify libraries. |
| `language` | query | `string` | no | Library language. |
| `isAssessment` | query | `boolean` | no | Include assessment-ready libraries. |
| `archived` | query | `boolean` | no | Include archived libraries. |
| `industryType` | query | `string` | no | Industry type filter. |
| `template` | query | `boolean` | no | Filter template libraries. |
| `isAiInterview` | query | `boolean` | no | Filter AI interview libraries. |
| `limit` | query | `number` | no | Number of items to return. |
| `skip` | query | `number` | no | Number of items to skip. |
