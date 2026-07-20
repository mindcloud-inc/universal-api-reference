# Get Jobs with TalentLyft

Retrieves all jobs from TalentLyft.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/jobs`
- **Base URL:** `https://api.talentlyft.com`
- **Official documentation:** [Get Jobs](https://developers.talentlyft.com/customer-api-reference/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to return. |
| `perPage` | query | `number` | no | Number of results to return per page. |
| `contains` | query | `string` | no | Filter jobs whose title contains this value. |
| `sort` | query | `string` | no | Sort order for the jobs list. |
| `details` | query | `boolean` | no | Whether to include job details and description fields. |
| `includeStages` | query | `boolean` | no | Whether to include job stages in each result. |
