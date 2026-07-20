# Resume Paused Lead with lemlist

Resumes a paused lead in lemlist.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/start/:leadId`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Resume Paused Lead](https://developer.lemlist.com/api-reference/endpoints/leads/resume-paused-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | The ID of the lead to resume. |
| `campaignId` | query | `string` | no | Resume the lead only in this specific campaign. |
