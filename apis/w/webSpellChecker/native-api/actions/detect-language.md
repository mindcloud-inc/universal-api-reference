# Detect Language with WebSpellChecker

Finds likely languages for text in WebSpellChecker.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://svc.webspellchecker.net/api`
- **Official documentation:** [Detect Language](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Detect%2Blanguage%2Bcommand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | The text to analyze for language detection. |
