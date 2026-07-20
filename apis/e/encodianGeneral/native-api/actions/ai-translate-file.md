# AI Translate File with Encodian - General

Translates a file to a target language with Encodian AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AITranslateFile`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Translate File](https://support.encodian.com/hc/en-gb/articles/13790274285724)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | Source filename including extension. |
| `fileContent` | body | `string` | yes | Base64-encoded source file content. |
| `targetLanguage` | body | `string` | yes | Language to translate the file into. |
