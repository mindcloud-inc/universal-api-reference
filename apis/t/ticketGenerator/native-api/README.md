# Ticket Generator: Native API Reference

A consolidated summary of Ticket Generator's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://apis.ticket-generator.com/client/api-docs/
- **API base URL:** `https://apis.ticket-generator.com/client`

## Authentication

### API Key

Connect with a Ticket Generator API key/certificate created from the Ticket Generator dashboard API section.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://support.ticket-generator.com/hc/en-us/articles/35493399663257-API-Key-Certificate)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ticket QR Data](actions/create-ticket-qr-data.md) | `POST v1/ticket/data/` | [docs](https://apis.ticket-generator.com/client/api-docs/) |
| [Create Ticket URL](actions/create-ticket-url.md) | `POST v1/ticket/url/` | [docs](https://apis.ticket-generator.com/client/api-docs/) |
| [Get Event Details](actions/get-event-details.md) | `GET v1/event/details/` | [docs](https://apis.ticket-generator.com/client/api-docs/) |
| [Send Ticket](actions/send-ticket.md) | `POST v1/ticket/send/` | [docs](https://apis.ticket-generator.com/client/api-docs/) |
