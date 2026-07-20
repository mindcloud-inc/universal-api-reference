# Create Question with RapidoForm

Creates a new question in RapidoForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/question`
- **Base URL:** `https://www.rapidoform.com/be`
- **Official documentation:** [Create Question](https://www.rapidoform.com/developers/docs/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `questionDescription` | body | `string` | yes |
| `questionOrder` | body | `number` | yes |
| `questionText` | body | `string` | yes |
| `questionType` | body | `string` | no |
| `surveyId` | body | `string` | yes |
