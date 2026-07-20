# Compress PDF with XSS PDF Solutions

Creates a compressed PDF in XSS PDF Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/29`
- **Base URL:** `https://api.xss-cross-service-solutions.com/solutions/solutions`
- **Official documentation:** [Compress PDF](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#compress-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The PDF file to compress. |
| `dpi` | body | `number` | yes | Dots per inch from 72 to 300. Smaller values reduce file size and quality. |
| `imageQuality` | body | `number` | yes | Image quality percentage from 0 to 100. Smaller values reduce file size and quality. |
