# Configure Multi Choice Nominal Question with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/question/updateQuestion`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Configure Multi Choice Nominal Question](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey containing the question to configure. |
| `questionId` | body | `string` | yes | Question to update. |
| `questionText` | body | `string` | yes | Prompt shown to respondents. |
| `optionsPayload` | body | `string` | yes | Option list for the nominal question. |
