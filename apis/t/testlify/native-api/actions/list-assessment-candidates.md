# List Assessment Candidates with Testlify

Retrieves candidates for a specific Testlify assessment.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/assessment/:assessmentId/candidate`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Assessment Candidates](https://docs.testlify.com/reference/get_all_candidates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assessmentId` | path | `string` | yes | Assessment identifier. |
| `query` | query | `string` | no | Search query string. |
| `candidateStatus` | query | `string` | no | Filter by candidate status. |
| `candidateStage` | query | `string` | no | Filter by candidate stage. |
| `invitationType` | query | `string` | no | Filter by invitation type. |
| `grade` | query | `string` | no | Filter by grade. |
| `completedRange` | query | `string` | no | Filter by completion time range. |
| `invitedBy` | query | `string` | no | Filter by inviter. |
| `workspaceLabelTitle` | query | `string` | no | Filter by workspace label title. |
| `colName` | query | `string` | no | Column name to sort by. |
| `inOrder` | query | `string` | no | Sort order. |
| `limit` | query | `number` | no | Number of items to return. |
| `skip` | query | `number` | no | Number of items to skip. |
