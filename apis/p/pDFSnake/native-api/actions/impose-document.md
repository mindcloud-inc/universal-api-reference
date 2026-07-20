# Impose Document with PDF Snake

Creates an imposed document from uploaded files in PDF Snake.

## Endpoint

- **Method:** `POST`
- **Path:** `/impose`
- **Base URL:** `https://api2.pdfsnake.app/api/v2`
- **Official documentation:** [Impose Document](https://api.swaggerhub.com/apis/R7274/PDFSnakeWebApi/6.227.0?resolved=true)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc` | body | `file` | yes | The PDF, JPEG, or PNG document to impose. |
| `steps` | body | `file` | yes | Upload the PDF Snake steps.json file. An empty JSON array (`[]`) is valid for a minimal passthrough imposition. |
| `overlay` | body | `file` | no | Optional overlay PDF used when the steps.json contains an Overlay step. |
| `insert` | body | `file` | no | Optional insert PDF used when the steps.json contains an Insert Pages step. |
