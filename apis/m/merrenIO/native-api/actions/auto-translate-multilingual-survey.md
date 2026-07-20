# Auto Translate Multilingual Survey with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/checkAllowTranslation`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Auto Translate Multilingual Survey](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey to translate. |
| `sourceLanguage` | body | `string` | yes | Current language of the survey. |
| `selectedLanguages` | body | `string` | yes | Languages Merren should translate the survey into. |
