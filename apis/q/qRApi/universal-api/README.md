# <img src="https://images.mindcloud.co/apps/icons/q-rapi_1776783184126.png" alt="QR Api logo" width="28" height="28"> QR Api: Universal API

Generate static QR codes for URLs, text, vCards, WiFi networks, map locations, phone calls, email, and SMS using QR Api's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qRApi/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://qrapi.io
- **Vendor API docs:** https://qrapi.io/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Email QR Code](actions/create-email-qr-code.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-email-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "hello@example.com"
}'
```

## Actions (8)

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Create Email QR Code](actions/create-email-qr-code.md) | POST | Creates a QR code for an email address in QR Api. |
| [Create Google Maps QR Code](actions/create-google-maps-qr-code.md) | POST | Creates a QR code for a Google Maps location in QR Api. |
| [Create Phone Call QR Code](actions/create-phone-call-qr-code.md) | POST | Creates a QR code for a phone call in QR Api. |
| [Create SMS QR Code](actions/create-sms-qr-code.md) | POST | Creates a QR code for a prefilled SMS in QR Api. |
| [Create Text QR Code](actions/create-text-qr-code.md) | POST | Creates a QR code for plain text in QR Api. |
| [Create URL QR Code](actions/create-url-qr-code.md) | POST | Creates a QR code for a URL in QR Api. |
| [Create VCard QR Code](actions/create-vcard-qr-code.md) | POST | Creates a QR code for a vCard in QR Api. |
| [Create WiFi QR Code](actions/create-wifi-qr-code.md) | POST | Creates a QR code for Wi-Fi access in QR Api. |

