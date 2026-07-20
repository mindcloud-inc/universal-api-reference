# Generate PDF from HTML with HTML to PDF

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/generate`
- **Base URL:** `https://platform.htmltopdfapi.co/api/v1`
- **Official documentation:** [Generate PDF from HTML](https://platform.htmltopdfapi.co/docs/api#/GeneratePdf/post_pdf_generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | yes | HTML markup to convert into a PDF document. |
| `filename` | body | `string` | no | Optional filename to suggest for the generated PDF. |
| `paper_size` | body | `string` | no | Optional paper size for the generated PDF. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `orientation` | body | `string` | no | Optional page orientation for the generated PDF. Accepted values: `0`, `1`. |
| `download` | body | `boolean` | no | When true, request a downloadable PDF response. |
