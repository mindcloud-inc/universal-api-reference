# Download Result Attachment with Startquestion

Downloads a survey response attachment from Startquestion.

## Endpoint

- **Method:** `GET`
- **Path:** `https://app.startquestion.com/api/v2/results/:surveyId/fill/:fillId/attachment/:questionId`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Download Result Attachment](https://help.startquestion.com/en/articles/5810324-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | Survey ID. |
| `fillId` | path | `number` | yes | Fill ID. |
| `questionId` | path | `number` | yes | Attachment question ID. |
