# PDF Unlock with Encodian

Unlocks a PDF document in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/UnlockPdfDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Unlock](https://support.encodian.com/hc/en-gb/articles/360003714237)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The PDF filename including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be unlocked. |
| `Password` | body | `string` | yes | The password used to unlock the document. |
