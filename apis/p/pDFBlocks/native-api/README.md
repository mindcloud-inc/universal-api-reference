# PDF Blocks: Native API Reference

A consolidated summary of PDF Blocks's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.pdfblocks.com/docs/api
- **OpenAPI specification:** https://www.pdfblocks.com/assets/specs/pdfblocks.openapi.yaml
- **API base URL:** `https://api.pdfblocks.com`

## Authentication

### API Key

Authenticate PDF Blocks API requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.pdfblocks.com/docs/api/getting-started)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Image Watermark](actions/add-image-watermark.md) | `POST /v1/add_watermark/image` | [docs](https://www.pdfblocks.com/docs/api/add-image-watermark-to-pdf) |
| [Add Password](actions/add-password.md) | `POST /v1/add_password` | [docs](https://www.pdfblocks.com/docs/api/add-password-to-pdf) |
| [Add Restrictions](actions/add-restrictions.md) | `POST /v1/add_restrictions` | [docs](https://www.pdfblocks.com/docs/api/add-restrictions-to-pdf) |
| [Add Text Watermark](actions/add-text-watermark.md) | `POST /v1/add_watermark/text` | [docs](https://www.pdfblocks.com/docs/api/add-text-watermark-to-pdf) |
| [Extract Pages](actions/extract-pages.md) | `POST /v1/extract_pages` | [docs](https://www.pdfblocks.com/docs/api/extract-pages-from-pdf) |
| [Merge Documents](actions/merge-documents.md) | `POST /v1/merge_documents` | [docs](https://www.pdfblocks.com/docs/api/merge-pdf-documents) |
| [Remove Pages](actions/remove-pages.md) | `POST /v1/remove_pages` | [docs](https://www.pdfblocks.com/docs/api/remove-pages-from-pdf) |
| [Remove Password](actions/remove-password.md) | `POST /v1/remove_password` | [docs](https://www.pdfblocks.com/docs/api/remove-password-from-pdf) |
| [Remove Restrictions](actions/remove-restrictions.md) | `POST /v1/remove_restrictions` | [docs](https://www.pdfblocks.com/docs/api/remove-restrictions-from-pdf) |
| [Remove Signatures](actions/remove-signatures.md) | `POST /v1/remove_signatures` | [docs](https://www.pdfblocks.com/docs/api/remove-signatures-from-pdf) |
| [Reverse Pages](actions/reverse-pages.md) | `POST /v1/reverse_pages` | [docs](https://www.pdfblocks.com/docs/api/reverse-pages-of-pdf) |
| [Rotate Pages](actions/rotate-pages.md) | `POST /v1/rotate_pages` | [docs](https://www.pdfblocks.com/docs/api/rotate-pages-in-pdf) |
