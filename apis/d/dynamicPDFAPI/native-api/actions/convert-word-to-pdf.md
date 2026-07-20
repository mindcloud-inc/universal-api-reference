# Convert Word To PDF with DynamicPDF

Converts a Word document to a PDF in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/pdf`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Convert Word To PDF](https://dpdf.io/docs/convert-word-to-pdf)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Instructions` | body | `file` | yes | DynamicPDF instructions JSON uploaded as the Instructions multipart part. |
| `Resource` | body | `file` | yes | Word document uploaded to DynamicPDF as a Resource part. |
