# Convert HTML to PDF with Plumsail Documents

Converts HTML to PDF in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/html-to-pdf`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert HTML to PDF](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Size` | body | `string` | no | Page size for the generated PDF. |
| `Orientation` | body | `string` | no | Page orientation for the generated PDF. |
| `Margins` | body | `string` | no | Margins definition for the generated PDF. |
| `Header` | body | `file` | no | Header HTML file to upload. |
| `Footer` | body | `file` | no | Footer HTML file to upload. |
| `HeaderUrl` | body | `string` | no | Anonymous URL to a header HTML file. |
| `FooterUrl` | body | `string` | no | Anonymous URL to a footer HTML file. |
| `File` | body | `file` | no | HTML file to convert into PDF. |
| `FileUrl` | body | `string` | no | Anonymous URL to an HTML file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
