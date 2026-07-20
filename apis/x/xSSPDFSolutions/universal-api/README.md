# <img src="https://images.mindcloud.co/apps/icons/cross-service-solutions_1777314513419.png" alt="XSS PDF Solutions logo" width="28" height="28"> XSS PDF Solutions: Universal API

PDF document automation tools from Cross Service Solutions, including PDF merge, compression, conversion, protection, unlocking, metadata removal, flattening, and AI question answering.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xSSPDFSolutions/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://login.cross-service-solutions.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ask PDF With AI](actions/ask-pdf-with-ai.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xSSPDFSolutions/latest/actions/ask-pdf-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "Upload a PDF, or use the default sample PDF URL.",
  "questtext": "Ask a question about the PDF."
}'
```

## Actions (8)

### Compressed Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Compress PDF](actions/compress-pdf.md) | POST | Creates a compressed PDF in XSS PDF Solutions. |

### Converted Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Convert to PDF](actions/convert-to-pdf.md) | POST | Creates a PDF in XSS PDF Solutions. |

### Flattened Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Flatten PDF](actions/flatten-pdf.md) | POST | Creates a flattened PDF in XSS PDF Solutions. |

### Merged Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Merge Multiple PDFs](actions/merge-multiple-pd-fs.md) | POST | Creates a merged PDF in XSS PDF Solutions. |

### Pdf Ai Question

| Action | Method | Description |
| --- | --- | --- |
| [Ask PDF With AI](actions/ask-pdf-with-ai.md) | POST | Creates answers from a PDF in XSS PDF Solutions. |

### Pdf Without Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Remove Metadata from PDF](actions/remove-metadata-from-pdf.md) | POST | Creates a PDF without metadata in XSS PDF Solutions. |

### Protected Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Protect PDF](actions/protect-pdf.md) | POST | Creates a protected PDF in XSS PDF Solutions. |

### Unlocked Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Unlock PDF](actions/unlock-pdf.md) | POST | Creates an unlocked PDF in XSS PDF Solutions. |

