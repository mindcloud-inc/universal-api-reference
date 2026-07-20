# AI Translate Text Single with Encodian - General

Translates a text block with Encodian AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AITranslateText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Translate Text Single](https://support.encodian.com/hc/en-gb/articles/13568846675996)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to translate. |
| `targetLanguage` | body | `string` | yes | Language to translate the text into. |
