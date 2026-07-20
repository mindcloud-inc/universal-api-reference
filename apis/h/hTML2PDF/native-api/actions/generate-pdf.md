# Generate PDF with HTML 2 PDF

## Endpoint

- **Method:** `POST`
- **Path:** `/generate`
- **Base URL:** `https://api.html2pdf.app/v1`
- **Official documentation:** [Generate PDF](https://html2pdf.app/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | HTML markup or a public URL to convert into a PDF document. |
| `format` | body | `list` | no | Optional paper format for the generated PDF. Accepted values: `A0`, `A1`, `A2`, `A3`, `A4`, `A5`, `A6`, `Ledger`, `Legal`, `Letter`, `Tabloid`. |
| `landscape` | body | `boolean` | no | Render the pages in landscape orientation. |
| `filename` | body | `string` | no | Optional filename to suggest for the generated PDF. |
| `media` | body | `list` | no | Emulate the selected CSS media type while rendering. Accepted values: `print`, `screen`. |
| `scale` | body | `number` | no | Rendering scale factor for the output PDF. |
| `width` | body | `number` | no | Custom page width for the generated PDF. |
| `height` | body | `number` | no | Custom page height for the generated PDF. |
| `waitFor` | body | `number` | no | Milliseconds to wait before rendering the page. |
| `callBackUrl` | body | `string` | no | Optional webhook URL to notify when PDF generation is complete. |
| `state` | body | `string` | no | State value returned unchanged to the callback URL. |
| `marginTop` | body | `number` | no | Top margin in pixels. |
| `marginRight` | body | `number` | no | Right margin in pixels. |
| `marginBottom` | body | `number` | no | Bottom margin in pixels. |
| `marginLeft` | body | `number` | no | Left margin in pixels. |
| `headerTemplate` | body | `string` | no | Optional HTML template rendered in the PDF header. |
| `footerTemplate` | body | `string` | no | Optional HTML template rendered in the PDF footer. |
| `userPassword` | body | `string` | no | User password required to open the generated PDF. |
| `ownerPassword` | body | `string` | no | Owner password used for PDF permission controls. |
| `permissions` | body | `list<string>` | no | Optional PDF permissions to allow when encryption is enabled. Accepted values: `assemble`, `copy`, `edit`, `extract`, `fillform`, `modify`, `print`, `printbest`. Send multiple values as a array. |
