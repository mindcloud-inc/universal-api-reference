# List Survey Collectors with Drag'n Survey

Retrieves collectors for a Drag'n Survey survey.

## Endpoint

- **Method:** `GET`
- **Path:** `surveys/:surveyId/collectors`
- **Base URL:** `https://developer.dragnsurvey.com/api/v2.0.0`
- **Official documentation:** [List Survey Collectors](https://developer.dragnsurvey.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | no | The Drag'n Survey survey ID. |
| `title_contains` | query | `string` | no | Filter collectors whose title contains this text. |
