# <img src="https://images.mindcloud.co/apps/icons/ziper_1776802608132.png" alt="Ziper logo" width="28" height="28"> Ziper: Universal API

Send WhatsApp messages and manage Ziper API access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ziper/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ziper.io
- **Vendor API docs:** https://documenter.getpostman.com/view/2881191/VUqmvyob

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get QR Code](actions/get-qr-code.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziper/latest/actions/get-qr-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Buttons](actions/send-buttons.md) | POST | Sends a WhatsApp button message with Ziper. |
| [Send List And Sections](actions/send-list-and-sections.md) | POST | Sends a WhatsApp list message with sections using Ziper. |
| [Send Location](actions/send-location.md) | POST | Sends a WhatsApp location message with Ziper. |
| [Send Simple Text](actions/send-simple-text.md) | POST | Sends a plain text WhatsApp message with Ziper. |
| [Send Template Buttons](actions/send-template-buttons.md) | POST | Sends a WhatsApp template-button message with Ziper. |
| [Send VCard](actions/send-v-card.md) | POST | Sends a WhatsApp vCard message with Ziper. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a WhatsApp login QR code from Ziper. |

