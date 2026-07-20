# Manually Edit Translations with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/question/updateTranslationQustion`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Manually Edit Translations](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey containing the translation to edit. |
| `questionId` | body | `string` | yes | Question whose translation should be updated. |
| `languageType` | body | `string` | yes | Language to edit. |
| `translatedText` | body | `string` | yes | Replacement translation text. |
