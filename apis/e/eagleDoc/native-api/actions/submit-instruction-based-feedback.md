# Submit Instruction-Based Feedback with Eagle Doc

Creates instruction-based feedback in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/docu/learning/instructions`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Submit Instruction-Based Feedback](https://www.eagle-doc.com/en/documentation/human-feedback/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corrected` | body | `file` | yes | Corrected extraction JSON file |
| `instructions` | query | `string` | yes | Semicolon-separated extraction instructions |
| `overwrite` | query | `boolean` | no | Whether to overwrite old learnings for this document |
