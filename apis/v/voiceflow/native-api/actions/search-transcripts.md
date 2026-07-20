# Search Transcripts with Voiceflow

Finds transcripts in Voiceflow by project criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript/project/:projectId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Search Transcripts](https://docs.voiceflow.com/api-reference/transcript/search-transcripts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `take` | query | `number` | no | Maximum number of results to return. |
| `skip` | query | `number` | no | Number of results to skip. |
| `order` | query | `string` | no | Sort order for returned results. |
| `filters[]` | body | `array<object>` | no | Filter transcripts based on properties and evaluation results. |
| `endDate` | body | `string` | no | Only include transcripts started before this timestamp. |
| `sessionID` | body | `string` | no | Only include transcripts for this session. |
| `startDate` | body | `string` | no | Only include transcripts started after this timestamp. |
| `environmentID` | body | `string` | no | Only include transcripts for this environment. |
