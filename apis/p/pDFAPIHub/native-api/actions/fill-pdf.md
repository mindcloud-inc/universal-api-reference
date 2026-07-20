# Fill PDF with PDF API Hub

## Endpoint

- **Method:** `POST`
- **Path:** `/fill-pdf`
- **Base URL:** `https://api.prefillpdf.com`
- **Official documentation:** [Fill PDF](https://api.prefillpdf.com/docs#/PDF%20Tools/fill_pdf_endpoint_fill_pdf_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | Template identifier for the PDF to fill. |
| `data` | body | `object` | no | Structured field values for detected template fields. |
| `form-fields` | body | `object` | no | Values for PDF AcroForm fields. |
| `images` | body | `object` | no | Mapping of image field keys to public image URLs. |
