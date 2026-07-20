# <img src="https://images.mindcloud.co/apps/icons/go-qrme_1776195052518.png" alt="goQR.me logo" width="28" height="28"> goQR.me: Universal API

Create and scan QR codes with goQR.me

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goQRme/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://goqr.me/
- **Vendor API docs:** https://goqr.me/api/doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Read QR Code](actions/read-qr-code.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/read-qr-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | POST | Creates a QR code with goQR.me. |
| [Read QR Code](actions/read-qr-code.md) | GET | Reads a QR code with goQR.me. |

