# Aloware: Native API Reference

A consolidated summary of Aloware's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://support.aloware.com/en/collections/8591828-webhooks
- **API base URL:** `https://app.aloware.com`

## Authentication

### API Token

Connect with an Aloware admin user's API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.aloware.com/en/articles/9020062-aloware-contact-lookup-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clear Power Dialer List](actions/clear-power-dialer-list.md) | `POST /api/v1/webhook/powerdialer-clear-list` | [docs](https://support.aloware.com/en/articles/9167815-aloware-power-dialer-apis) |
| [Clear User Power Dialer Lists](actions/clear-user-power-dialer-lists.md) | `POST /api/v1/webhook/powerdialer-clear-user-lists` | [docs](https://support.aloware.com/en/articles/9167815-aloware-power-dialer-apis) |
| [Create Contact](actions/create-contact.md) | `POST /api/v1/webhook/forms` | [docs](https://support.aloware.com/en/articles/9020058-aloware-lead-api-documentation) |
| [Disenroll Contact From Sequences](actions/disenroll-contact-from-sequences.md) | `POST /api/v1/webhook/sequence-disenroll` | [docs](https://support.aloware.com/en/articles/9020073-aloware-sequence-api-enroll-and-disenroll-contacts-in-sequences) |
| [Enroll Contact In Sequence](actions/enroll-contact-in-sequence.md) | `POST /api/v1/webhook/sequence-enroll` | [docs](https://support.aloware.com/en/articles/9020073-aloware-sequence-api-enroll-and-disenroll-contacts-in-sequences) |
| [Establish Two-Legged Call](actions/establish-two-legged-call.md) | `POST /api/v1/webhook/two-legged-call` | [docs](https://support.aloware.com/en/articles/9019991-api-documentation-aloware-two-legged-call-api-integration) |
| [List Users](actions/list-users.md) | `GET /api/v1/webhook/users` | [docs](https://support.aloware.com/en/articles/9352647-api-documentation-users-api) |
| [Lookup Contact By Phone Number](actions/lookup-contact-by-phone-number.md) | `GET /api/v1/webhook/contact/phone-number` | [docs](https://support.aloware.com/en/articles/9020068-aloware-contact-lookup-api) |
| [Remove Contact From Power Dialer Lists](actions/remove-contact-from-power-dialer-lists.md) | `POST /api/v1/webhook/powerdialer-remove-contact-from-lists` | [docs](https://support.aloware.com/en/articles/9167815-aloware-power-dialer-apis) |
| [Send SMS](actions/send-sms.md) | `POST /api/v1/webhook/sms-gateway/send` | [docs](https://support.aloware.com/en/articles/9020040-api-documentation-aloware-sms-api-integration) |
| [Update Contact](actions/update-contact.md) | `POST /api/v1/webhook/forms` | [docs](https://support.aloware.com/en/articles/9020058-aloware-lead-api-documentation) |
