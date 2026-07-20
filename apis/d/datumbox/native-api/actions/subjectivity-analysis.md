# Subjectivity Analysis with Datumbox

Analyzes a document's subjectivity in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/SubjectivityAnalysis.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Subjectivity Analysis](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to evaluate for subjectivity. |
