# Get Interviews with Mona AI

Retrieves interviews from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/database/getInterviewsFromDatabase`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Interviews](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional interview filters such as status, interviewType, applicantId, jobOfferId, and interviewer. |
| `paginationToken` | body | `string` | no | Provider pagination token for additional results. |
| `sort` | body | `object` | no | Optional interview sort object with field and direction. |
