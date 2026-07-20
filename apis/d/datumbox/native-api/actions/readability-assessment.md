# Readability Assessment with Datumbox

Assesses a document's readability in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/ReadabilityAssessment.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Readability Assessment](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to evaluate for readability. |
