# PDF Delete Pages with Encodian

Deletes PDF pages in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/DeletePdfPages`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Delete Pages](https://support.encodian.com/hc/en-gb/articles/13690317983132/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContent` | body | `string` | yes | The file content of the source PDF file. |
| `StartPage` | body | `string` | no | Set the page number to begin deleting pages from. |
| `EndPage` | body | `string` | no | Set the page number to stop deleting pages on. |
| `PageNumbers` | body | `string` | no | A comma separated list of page numbers to delete, for example 1,3,4. |
