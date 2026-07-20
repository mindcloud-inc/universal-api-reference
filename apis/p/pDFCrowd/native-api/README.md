# PDFCrowd: Native API Reference

A consolidated summary of PDFCrowd's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://pdfcrowd.com/api/
- **API base URL:** `https://api.pdfcrowd.com/convert/24.04/`

## Authentication

### Basic Auth

Use your PDFCrowd API username and API key. PDFCrowd requires standard HTTP Basic authentication with username:apikey.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://pdfcrowd.com/api/html-to-pdf-http/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Combine PDF Files](actions/combine-pdf-files.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-pdf-http/ref/) |
| [Convert HTML File to Image](actions/convert-html-file-to-image.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/html-to-image-http/ref/) |
| [Convert HTML File to PDF](actions/convert-html-file-to-pdf.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/html-to-pdf-http/ref/) |
| [Convert HTML String to Image](actions/convert-html-string-to-image.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/html-to-image-http/ref/) |
| [Convert HTML String to PDF](actions/convert-html-string-to-pdf.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/html-to-pdf-http/ref/) |
| [Convert Image File to Image](actions/convert-image-file-to-image.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/image-to-image-http/ref/) |
| [Convert Image File to PDF](actions/convert-image-file-to-pdf.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/image-to-pdf-http/ref/) |
| [Convert Image URL to Image](actions/convert-image-url-to-image.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/image-to-image-http/ref/) |
| [Convert Image URL to PDF](actions/convert-image-url-to-pdf.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/image-to-pdf-http/ref/) |
| [Convert PDF File to HTML](actions/convert-pdf-file-to-html.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-html-http/ref/) |
| [Convert PDF File to Image](actions/convert-pdf-file-to-image.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-image-http/ref/) |
| [Convert PDF File to Text](actions/convert-pdf-file-to-text.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-text-http/ref/) |
| [Convert PDF URL to HTML](actions/convert-pdfurl-to-html.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-html-http/ref/) |
| [Convert PDF URL to Image](actions/convert-pdfurl-to-image.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-image-http/ref/) |
| [Convert PDF URL to Text](actions/convert-pdfurl-to-text.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-text-http/ref/) |
| [Convert URL to Image](actions/convert-url-to-image.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/html-to-image-http/ref/) |
| [Convert URL to PDF](actions/convert-url-to-pdf.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/html-to-pdf-http/ref/) |
| [Delete PDF Pages](actions/delete-pdf-pages.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-pdf-http/ref/) |
| [Extract PDF Pages](actions/extract-pdf-pages.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-pdf-http/ref/) |
| [Shuffle PDF Files](actions/shuffle-pdf-files.md) | `POST https://api.pdfcrowd.com/convert/24.04/` | [docs](https://pdfcrowd.com/api/pdf-to-pdf-http/ref/) |
