# Educational Detection with Datumbox

Detects educational intent in a document with Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/EducationalDetection.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Educational Detection](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to evaluate for educational intent. |
