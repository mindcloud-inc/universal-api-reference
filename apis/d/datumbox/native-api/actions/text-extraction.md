# Text Extraction with Datumbox

Extracts clear text from HTML in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/TextExtraction.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Text Extraction](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The HTML source of the webpage to extract text from. |
