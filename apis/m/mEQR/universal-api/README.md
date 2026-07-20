# <img src="https://images.mindcloud.co/apps/icons/m-eqr_1773930104078.png" alt="ME-QR logo" width="28" height="28"> ME-QR: Universal API

Create, customize, and manage dynamic QR codes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mEQR/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://me-qr.com
- **Vendor API docs:** https://me-qr.com/api/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List QRs](actions/list-q-rs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/list-q-rs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Create Email QR](actions/create-email-qr.md) | POST | Creates an email QR code in ME-QR. |
| [Create File QR](actions/create-file-qr.md) | POST | Creates a file QR code in ME-QR. |
| [Create Gallery QR](actions/create-gallery-qr.md) | POST | Creates a gallery QR code in ME-QR. |
| [Create Link List QR](actions/create-link-list-qr.md) | POST | Creates a link list QR code in ME-QR. |
| [Create Link QR](actions/create-link-qr.md) | POST | Creates a link QR code in ME-QR. |
| [Create Map QR](actions/create-map-qr.md) | POST | Creates a map QR code in ME-QR. |
| [Create PDF QR](actions/create-pdfqr.md) | POST | Creates a PDF QR code in ME-QR. |
| [Create Phone QR](actions/create-phone-qr.md) | POST | Creates a phone QR code in ME-QR. |
| [Create Text QR](actions/create-text-qr.md) | POST | Creates a text QR code in ME-QR. |
| [Create vCard QR](actions/create-v-card-qr.md) | POST | Creates a vCard QR code in ME-QR. |
| [Create Video QR](actions/create-video-qr.md) | POST | Creates a video QR code in ME-QR. |
| [Create WhatsApp QR](actions/create-whats-app-qr.md) | POST | Creates a WhatsApp QR code in ME-QR. |
| [Create WiFi QR](actions/create-wi-fi-qr.md) | POST | Creates a WiFi QR code in ME-QR. |
| [Get Email QR](actions/get-email-qr.md) | GET | Retrieves an email QR code from ME-QR. |
| [Get File QR](actions/get-file-qr.md) | GET | Retrieves a file QR code from ME-QR. |
| [Get Gallery QR](actions/get-gallery-qr.md) | GET | Retrieves a gallery QR code from ME-QR. |
| [Get Link List QR](actions/get-link-list-qr.md) | GET | Retrieves a link list QR code from ME-QR. |
| [Get Link QR](actions/get-link-qr.md) | GET | Retrieves a link QR code from ME-QR. |
| [Get Map QR](actions/get-map-qr.md) | GET | Retrieves a map QR code from ME-QR. |
| [Get PDF QR](actions/get-pdfqr.md) | GET | Retrieves a PDF QR code from ME-QR. |
| [Get Phone QR](actions/get-phone-qr.md) | GET | Retrieves a phone QR code from ME-QR. |
| [Get Text QR](actions/get-text-qr.md) | GET | Retrieves a text QR code from ME-QR. |
| [Get vCard QR](actions/get-v-card-qr.md) | GET | Retrieves a vCard QR code from ME-QR. |
| [Get Video QR](actions/get-video-qr.md) | GET | Retrieves a video QR code from ME-QR. |
| [Get WhatsApp QR](actions/get-whats-app-qr.md) | GET | Retrieves a WhatsApp QR code from ME-QR. |
| [Get WiFi QR](actions/get-wi-fi-qr.md) | GET | Retrieves a WiFi QR code from ME-QR. |
| [List QRs](actions/list-q-rs.md) | GET | Retrieves all QR codes from ME-QR. |
| [Update Email QR](actions/update-email-qr.md) | PUT | Updates an email QR code in ME-QR. |
| [Update File QR](actions/update-file-qr.md) | PUT | Updates a file QR code in ME-QR. |
| [Update Gallery QR](actions/update-gallery-qr.md) | PUT | Updates a gallery QR code in ME-QR. |
| [Update Link List QR](actions/update-link-list-qr.md) | PUT | Updates a link list QR code in ME-QR. |
| [Update Link QR](actions/update-link-qr.md) | PUT | Updates a link QR code in ME-QR. |
| [Update Map QR](actions/update-map-qr.md) | PUT | Updates a map QR code in ME-QR. |
| [Update PDF QR](actions/update-pdfqr.md) | PUT | Updates a PDF QR code in ME-QR. |
| [Update Phone QR](actions/update-phone-qr.md) | PUT | Updates a phone QR code in ME-QR. |
| [Update Text QR](actions/update-text-qr.md) | PUT | Updates a text QR code in ME-QR. |
| [Update vCard QR](actions/update-v-card-qr.md) | PUT | Updates a vCard QR code in ME-QR. |
| [Update Video QR](actions/update-video-qr.md) | PUT | Updates a video QR code in ME-QR. |
| [Update WhatsApp QR](actions/update-whats-app-qr.md) | PUT | Updates a WhatsApp QR code in ME-QR. |
| [Update WiFi QR](actions/update-wi-fi-qr.md) | PUT | Updates a WiFi QR code in ME-QR. |

