# Create Survey Collector with Drag'n Survey

Creates a collector for a Drag'n Survey survey.

## Endpoint

- **Method:** `POST`
- **Path:** `surveys/:surveyId/collectors`
- **Base URL:** `https://developer.dragnsurvey.com/api/v2.0.0`
- **Official documentation:** [Create Survey Collector](https://developer.dragnsurvey.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | no | The Drag'n Survey survey ID. |
| `title` | body | `string` | yes | Collector title. |
