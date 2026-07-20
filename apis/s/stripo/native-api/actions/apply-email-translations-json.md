# Apply Email Translations JSON with Stripo

Applies email translations from a JSON file in Stripo.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:id/translation-versions/json/apply`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Apply Email Translations JSON](https://api.stripo.email/reference/applyemailtranslationjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | JSON file containing translation data. |
| `id` | path | `number` | yes | The email ID. |
| `targetLanguages[]` | body | `array<string>` | yes | Target language codes in locale format. Send multiple values as a array. |
