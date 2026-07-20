# List Assessments with Testlify

Retrieves assessments from Testlify with optional filters and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/assessment`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Assessments](https://docs.testlify.com/reference/get_all_assessments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search query string. |
| `groupName` | query | `string` | no | Group name to filter assessments. |
| `workspaceLabelTitle` | query | `string` | no | Workspace label title. |
| `isActive` | query | `boolean` | no | Filter active assessments. |
| `isArchived` | query | `boolean` | no | Filter archived assessments. |
| `isEditable` | query | `boolean` | no | Filter editable assessments. |
| `isDraft` | query | `boolean` | no | Filter draft assessments. |
| `colName` | query | `string` | no | Column name to sort by. |
| `inOrder` | query | `string` | no | Sort order. |
| `limit` | query | `number` | no | Number of items to return. |
| `skip` | query | `number` | no | Number of items to skip. |
