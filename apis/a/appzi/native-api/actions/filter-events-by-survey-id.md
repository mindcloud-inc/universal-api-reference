# Filter Events By Survey ID with Appzi

Retrieves a survey event filter snippet from Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/integration/events/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Filter Events By Survey ID](https://docs.appzi.io/integration/events/#filter-events-by-survey-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configId` | query | `string` | yes | The Appzi survey configuration ID to match in evt.surveyId. |
