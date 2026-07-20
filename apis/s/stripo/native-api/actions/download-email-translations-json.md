# Download Email Translations JSON with Stripo

Downloads email translations as a JSON file from Stripo.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:id/translation-versions/json`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Download Email Translations JSON](https://api.stripo.email/reference/createemailtranslationjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The email ID. |
| `targetLanguages[]` | body | `array<string>` | yes | Target language codes in locale format. Send multiple values as a array. |
