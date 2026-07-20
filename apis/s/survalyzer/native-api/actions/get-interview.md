# Get Interview with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Interview/v3/ReadInterview`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Get Interview](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant` | body | `string` | yes | Tenant code for the interview request. |
| `surveyId` | body | `number` | yes | Survey identifier that owns the interview. |
| `interviewId` | body | `string` | yes | Interview identifier to read. |
| `loadSurveyDefinition` | body | `boolean` | no | Whether to include survey definition in the response. |
