# Submit Corrected Extraction Feedback with Eagle Doc

Creates corrected extraction feedback in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/docu/learning`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Submit Corrected Extraction Feedback](https://www.eagle-doc.com/en/documentation/human-feedback/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corrected` | body | `file` | yes | Corrected extraction JSON file |
| `file` | body | `file` | yes | Original document file used for extraction |
| `original` | body | `file` | yes | Original extraction JSON file |
