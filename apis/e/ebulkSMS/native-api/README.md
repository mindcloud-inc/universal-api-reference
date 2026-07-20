# EbulkSMS: Native API Reference

A consolidated summary of EbulkSMS's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.ebulksms.com/pages/api-docs
- **API base URL:** `https://api.ebulksms.com`

## Authentication

### API Key

Use your EbulkSMS login email and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · Your EbulkSMS login email address.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ebulksms.com/pages/api-docs)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | `GET /balance/:username/:apiKey` | [docs](https://www.ebulksms.com/pages/get-api) |
| [Get API Key](actions/get-api-key.md) | `POST /getapikey.json` | [docs](https://www.ebulksms.com/files/uploads/docs/ebulksms-api.pdf) |
| [Get SMS Delivery Reports](actions/get-sms-delivery-reports.md) | `GET /getdlr.json` | [docs](https://www.ebulksms.com/files/uploads/docs/ebulksms-api.pdf) |
| [Get WhatsApp Delivery Reports](actions/get-whatsapp-delivery-reports.md) | `GET /getwadlr.json` | [docs](https://www.ebulksms.com/files/uploads/docs/ebulksms-api.pdf) |
| [Send SMS](actions/send-sms.md) | `POST /sendsms.json` | [docs](https://www.ebulksms.com/pages/json-api) |
