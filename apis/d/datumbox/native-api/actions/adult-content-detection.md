# Adult Content Detection with Datumbox

Detects adult content in a document with Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/AdultContentDetection.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Adult Content Detection](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to evaluate for adult-content detection. |
