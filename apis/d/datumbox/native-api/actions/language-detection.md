# Language Detection with Datumbox

Detects a document's language in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/LanguageDetection.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Language Detection](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to evaluate. |
