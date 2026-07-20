# Get Applicants with Mona AI

Retrieves applicants from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/database/getApplicantsFromDatabase`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Applicants](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional applicant filters such as jobId and status. |
| `limit` | body | `number` | no | Maximum applicants to return. |
| `page` | body | `number` | no | Page number to retrieve. |
| `sort` | body | `object` | no | Optional sort object with field and direction. |
