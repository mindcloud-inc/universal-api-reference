# Get Vendor Questionnaire Questions And Answers with UpGuard

Retrieves questionnaire questions and answers from UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/questionnaire/answers`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Get Vendor Questionnaire Questions And Answers](https://cyber-risk.upguard.com/api/docs#operation/questionnaireAnswers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | The numeric ID of the questionnaire whose answers should be returned. |
