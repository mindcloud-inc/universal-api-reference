# Get Matching Results with Mona AI

Retrieves applicant matching results from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/matching/getMatchingResults`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Matching Results](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantId` | body | `string` | no | Applicant identifier to filter matching results. |
| `jobOfferId` | body | `string` | no | Job offer identifier to filter matching results. |
| `limit` | body | `number` | no | Maximum matching results to return. |
| `paginationToken` | body | `string` | no | Provider pagination token for additional matching results. |
