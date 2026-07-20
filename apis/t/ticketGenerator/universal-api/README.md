# <img src="https://images.mindcloud.co/apps/icons/ticket-generator_1774909503190.png" alt="Ticket Generator logo" width="28" height="28"> Ticket Generator: Universal API

Ticket Generator helps teams generate secure event tickets with QR codes, ticket images, and direct delivery through its API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ticketGenerator/latest
- **Category:** Support / Ticketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ticket-generator.com
- **Vendor API docs:** https://apis.ticket-generator.com/client/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Event Details](actions/get-event-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketGenerator/latest/actions/get-event-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Details](actions/get-event-details.md) | GET | Retrieves active event details and ticket categories from Ticket Generator. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket QR Data](actions/create-ticket-qr-data.md) | POST | Creates ticket QR code data and ticket ID in Ticket Generator. |
| [Create Ticket URL](actions/create-ticket-url.md) | POST | Creates a QR code ticket URL in Ticket Generator. |
| [Send Ticket](actions/send-ticket.md) | POST | Sends a ticket by email, SMS, or WhatsApp in Ticket Generator. |

