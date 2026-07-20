# PDF Delete Pages with PDF.co

Deletes pages from a PDF in PDF.co.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/edit/delete-pages`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [PDF Delete Pages](https://docs.pdf.co/api-tester/pdf-delete-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source PDF URL. |
| `pages` | body | `string` | yes | Page range to delete, e.g. 1,3-5. |
| `async` | body | `boolean` | no | Set true to run as async job. |
