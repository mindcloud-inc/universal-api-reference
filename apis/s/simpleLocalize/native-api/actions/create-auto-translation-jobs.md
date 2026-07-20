# Create Auto-Translation Jobs with SimpleLocalize

Creates auto-translation jobs in SimpleLocalize.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/jobs/auto-translate`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Create Auto-Translation Jobs](https://api.simplelocalize.io/openapi/ui#/Auto-translation/autoTranslate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageKeys[]` | body | `array<string>` | no | Project source language keys, if not provided then all languages will be translated. Auto-translation configuration will be used from the last auto-translation job. |
| `options` | body | `list<string>` | no | Options for auto-translation Accepted values: `FORCE_REPLACE`, `USE_TRANSLATION_KEYS`. |
