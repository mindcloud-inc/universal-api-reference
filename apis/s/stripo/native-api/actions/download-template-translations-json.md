# Download Template Translations JSON with Stripo

Downloads template translations as a JSON file from Stripo.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:id/translation-versions/json`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Download Template Translations JSON](https://api.stripo.email/reference/createtemplatetranslationjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The template ID. |
| `targetLanguages[]` | body | `array<string>` | yes | Target language codes in locale format. Send multiple values as a array. |
