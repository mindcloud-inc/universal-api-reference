# Generate PDF from URL with HTML to PDF

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf/generate`
- **Base URL:** `https://platform.htmltopdfapi.co/api/v1`
- **Official documentation:** [Generate PDF from URL](https://platform.htmltopdfapi.co/docs/api#/GeneratePdf/post_pdf_generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL whose rendered content should be converted into a PDF. |
| `filename` | body | `string` | no | Optional filename to suggest for the generated PDF. |
| `paper_size` | body | `string` | no | Optional paper size for the generated PDF. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `orientation` | body | `string` | no | Optional page orientation for the generated PDF. Accepted values: `0`, `1`. |
| `download` | body | `boolean` | no | When true, request a downloadable PDF response. |
