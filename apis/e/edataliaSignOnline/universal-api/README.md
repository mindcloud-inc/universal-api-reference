# <img src="https://images.mindcloud.co/apps/icons/firmar-online-home-1_1777486303637.png" alt="edatalia Sign Online logo" width="28" height="28"> edatalia Sign Online: Universal API

edatalia Sign Online provides REST APIs for creating and managing digital signature envelopes, retrieving signed documents and evidence, applying server-side electronic signatures and timestamps, and validating signed PDFs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/edataliaSignOnline/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://firmar.online/
- **Vendor API docs:** https://edatalia.com/kb/api-rest-40/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Devices](actions/list-devices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Audit Trail

| Action | Method | Description |
| --- | --- | --- |
| [Get Envelope Audit Trail](actions/get-envelope-audit-trail.md) | GET | Retrieves an envelope audit trail from edatalia Sign Online. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves available devices from edatalia Sign Online. |

### Electronic Signature

| Action | Method | Description |
| --- | --- | --- |
| [Sign PDF With Certificate](actions/sign-pdf-with-certificate.md) | POST | Signs a PDF with a certificate in edatalia Sign Online. |

### Envelope

| Action | Method | Description |
| --- | --- | --- |
| [Get Envelope Details](actions/get-envelope-details.md) | GET | Retrieves envelope details from edatalia Sign Online. |
| [Get Envelope Signing URL](actions/get-envelope-signing-url.md) | GET | Retrieves an envelope signing URL from edatalia Sign Online. |
| [Get Envelope Status](actions/get-envelope-status.md) | GET | Retrieves an envelope's status from edatalia Sign Online. |
| [List Signature History](actions/list-signature-history.md) | GET | Retrieves signature history from edatalia Sign Online. |
| [Search Envelopes By Reference](actions/search-envelopes-by-reference.md) | GET | Finds envelopes in edatalia Sign Online by external reference. |

### Evidence Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Envelope Evidence Document](actions/get-envelope-evidence-document.md) | GET | Retrieves an envelope evidence document from edatalia Sign Online. |

### Timestamped Signature

| Action | Method | Description |
| --- | --- | --- |
| [Timestamp Signed PDF](actions/timestamp-signed-pdf.md) | POST | Adds a timestamp to a signed PDF in edatalia Sign Online. |

