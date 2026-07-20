# Randomize Multiple Choice Options with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/question/updateQuestion`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Randomize Multiple Choice Options](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey containing the question to randomize. |
| `questionId` | body | `string` | yes | Question to randomize. |
