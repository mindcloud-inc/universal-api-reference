# Fill PDF Form From Template ID With Custom Font Size with DocMaker

Creates a PDF form from a template ID with custom font size in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/fill_pdf`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Fill PDF Form From Template ID With Custom Font Size](https://guide.docmaker.co/features/fill-out-pdf-forms/pdf_fill-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `templateID` | body | `string` | yes |
| `data` | body | `object` | no |
| `fontSize` | body | `number` | yes |
