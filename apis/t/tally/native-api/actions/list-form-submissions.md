# List Form Submissions with Tally

## Endpoint

- **Method:** `GET`
- **Path:** `forms/:formId/submissions`
- **Base URL:** `https://api.tally.so`
- **Official documentation:** [List Form Submissions](https://developers.tally.so/api-reference/endpoint/forms/submissions/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<string>` | yes | — |
| `filter` | query | `list<string>` | no | Filter submissions by status |
| `startDate` | query | `date` | no | Filter submissions submitted on or after this date |
| `endDate` | query | `date` | no | Filter submissions submitted on or before this date |
| `afterId` | query | `string` | no | Get submissions that came after a specific submission ID |
