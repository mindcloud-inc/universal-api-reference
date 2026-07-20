# Smsmobileapi: Native API Reference

A consolidated summary of Smsmobileapi's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://smsmobileapi.com/documentations-api-smsmobileapi/
- **API base URL:** `https://api.smsmobileapi.com`

## Authentication

### API Key

Authenticate with your SMSMobileAPI API key. Provider endpoints accept the key as the apikey request parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://smsmobileapi.com/doc/)

## API conventions

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List API Sent SMS](actions/list-api-sent-sms.md) | `GET /log/sent/sms/` | [docs](https://smsmobileapi.com/doc/) |
| [List Connected Mobiles](actions/list-connected-mobiles.md) | `GET /gateway/mobile/list/` | [docs](https://smsmobileapi.com/doc/) |
| [List Missed Calls](actions/list-missed-calls.md) | `GET /call/missed/list/` | [docs](https://smsmobileapi.com/doc-call/) |
| [List Notifications](actions/list-notifications.md) | `GET /notification/list/` | [docs](https://smsmobileapi.com/doc-notification/) |
| [List SMS Conversations](actions/list-sms-conversations.md) | `GET /conversation/sms/list/` | [docs](https://smsmobileapi.com/doc/) |
| [Set WhatsApp Retrieval Status](actions/set-whatsapp-retrieval-status.md) | `GET /getwa/active/` | [docs](https://smsmobileapi.com/doc-whatsapp/) |
