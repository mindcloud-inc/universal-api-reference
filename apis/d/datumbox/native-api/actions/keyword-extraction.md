# Keyword Extraction with Datumbox

Extracts keywords from a document in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/KeywordExtraction.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Keyword Extraction](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to analyze for keyword extraction. |
| `n` | body | `number` | yes | The maximum keyword-combination size to extract. |
