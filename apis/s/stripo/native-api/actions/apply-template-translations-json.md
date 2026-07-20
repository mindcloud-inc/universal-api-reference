# Apply Template Translations JSON with Stripo

Applies template translations from a JSON file in Stripo.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:id/translation-versions/json/apply`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Apply Template Translations JSON](https://api.stripo.email/reference/applytemplatetranslationjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | JSON file containing translation data. |
| `id` | path | `number` | yes | The template ID. |
| `targetLanguages[]` | body | `array<string>` | yes | Target language codes in locale format. Send multiple values as a array. |
