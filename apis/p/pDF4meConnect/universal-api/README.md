# <img src="https://images.mindcloud.co/apps/icons/p-df4me-connect_1777575604952.png" alt="PDF4me Connect logo" width="28" height="28"> PDF4me Connect: Universal API

Run PDF4me document conversion, OCR, metadata extraction, generation, and PDF processing workflows from the PDF4me API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDF4meConnect/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.pdf4me.com/
- **Vendor API docs:** https://docs.pdf4me.com/pdf4me-api/getting-started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Credentials](actions/validate-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDF4meConnect/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Validate Credentials](actions/validate-credentials.md) | GET |  |

