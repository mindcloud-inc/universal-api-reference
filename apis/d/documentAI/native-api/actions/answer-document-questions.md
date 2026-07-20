# Answer Document Questions with Document AI

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/analyze/answer-questions`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Answer Document Questions](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-analyze-answer-questions-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `string` | yes | Base64-encoded document content to answer questions from. |
| `QuestionsYesNo[]` | body | `array<object>` | no | Yes/no questions to answer from the document. |
| `QuestionsMultipleChoice[]` | body | `array<object>` | no | Multiple-choice questions to answer from the document. |
| `QuestionsFreeResponse[]` | body | `array<object>` | no | Free-response questions to answer from the document. |
| `RecognitionMode` | body | `string` | no | OCR recognition mode. |
