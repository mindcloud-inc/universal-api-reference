# Create PDF from Webpage with DocMaker

Creates a PDF from a webpage in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/page_pdf`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Create PDF from Webpage](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `url` | body | `string` | yes |
| `pageSize` | body | `string` | yes |
| `loadTime` | body | `number` | no |
| `pageRanges` | body | `string` | no |
| `getBase64` | body | `boolean` | no |
| `landscape` | body | `boolean` | yes |
| `marginLeft` | body | `string` | no |
| `marginRight` | body | `string` | no |
| `marginTop` | body | `string` | no |
| `marginBottom` | body | `string` | no |
| `timeZone` | body | `string` | no |
| `language` | body | `string` | no |
| `vWidth` | body | `number` | no |
| `vHeight` | body | `number` | no |
| `showFooter` | body | `string` | no |
| `htmlFooter` | body | `string` | no |
| `upload_output_file` | body | `boolean` | no |
| `metadata` | body | `string` | no |
| `webhook_url` | body | `string` | no |
| `webhook_object_id` | body | `string` | no |
| `webhook_object_type` | body | `string` | no |
