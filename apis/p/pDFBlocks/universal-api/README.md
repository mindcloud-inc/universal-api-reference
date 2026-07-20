# <img src="https://images.mindcloud.co/apps/icons/p-dfblocks_1774624057555.png" alt="PDF Blocks logo" width="28" height="28"> PDF Blocks: Universal API

Process PDFs by merging, protecting, watermarking, and editing pages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFBlocks/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pdfblocks.com
- **Vendor API docs:** https://www.pdfblocks.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Add Image Watermark](actions/add-image-watermark.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-image-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "image": "string"
}'
```

## Actions (12)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Add Image Watermark](actions/add-image-watermark.md) | PUT | Updates a PDF document with an image watermark in PDF Blocks. |
| [Add Password](actions/add-password.md) | PUT | Updates a PDF document with a password in PDF Blocks. |
| [Add Restrictions](actions/add-restrictions.md) | PUT | Updates a PDF document with restrictions in PDF Blocks. |
| [Add Text Watermark](actions/add-text-watermark.md) | PUT | Updates a PDF document with a text watermark in PDF Blocks. |
| [Extract Pages](actions/extract-pages.md) | POST | Creates a PDF document with extracted pages in PDF Blocks. |
| [Merge Documents](actions/merge-documents.md) | POST | Creates a merged PDF document in PDF Blocks. |
| [Remove Pages](actions/remove-pages.md) | PUT | Updates a PDF document by removing pages in PDF Blocks. |
| [Remove Password](actions/remove-password.md) | PUT | Updates a PDF document by removing its password in PDF Blocks. |
| [Remove Restrictions](actions/remove-restrictions.md) | PUT | Updates a PDF document by removing restrictions in PDF Blocks. |
| [Remove Signatures](actions/remove-signatures.md) | PUT | Updates a PDF document by removing signatures in PDF Blocks. |
| [Reverse Pages](actions/reverse-pages.md) | PUT | Updates a PDF document by reversing page order in PDF Blocks. |
| [Rotate Pages](actions/rotate-pages.md) | PUT | Updates a PDF document by rotating pages in PDF Blocks. |

