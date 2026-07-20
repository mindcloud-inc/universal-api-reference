# <img src="https://images.mindcloud.co/apps/icons/valida-cfdi_1775064599406.png" alt="ValidaCFDI logo" width="28" height="28"> ValidaCFDI: Universal API

Validate CFDIs, extract invoice data, and verify supplier risk

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/validaCFDI/latest
- **Category:** Commerce / Accounting
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://valida-cfdi.com.mx
- **Vendor API docs:** https://valida-cfdi.com.mx/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Connection](actions/test-api-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/test-api-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Test API Connection](actions/test-api-connection.md) | GET | Tests the API connection in ValidaCFDI. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Validate CFDI by UUID](actions/validate-cfdi-by-uuid.md) | GET | Validates a CFDI by UUID in ValidaCFDI. |
| [Validate CFDI from PDF](actions/validate-cfdi-from-pdf.md) | GET | Validates a CFDI from a PDF in ValidaCFDI. |

