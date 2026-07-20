# <img src="https://images.mindcloud.co/apps/icons/qryptal_1775057643921.png" alt="Qryptal logo" width="28" height="28"> Qryptal: Universal API

Generate, verify, and manage secure QR codes and documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qryptal/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.qryptal.com/
- **Vendor API docs:** https://dash2.qryptal.com/docs/api2-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download QR Code Image](actions/download-qr-code-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/download-qr-code-image?connectionId=$CONNECTION_ID&uid=1097580178100010000601672116&codeToken=C02%3ArFKsq1dyUmJZZFNze1Jr..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Qryptal Qr Codes

| Action | Method | Description |
| --- | --- | --- |
| [Download QR Code Image](actions/download-qr-code-image.md) | GET |  |
| [Generate EDC QR Code With Attachments](actions/generate-edc-qr-code-with-attachments.md) | POST |  |
| [Generate PDC QR Code](actions/generate-pdc-qr-code.md) | POST |  |
| [Get QR Code Status](actions/get-qr-code-status.md) | GET |  |

