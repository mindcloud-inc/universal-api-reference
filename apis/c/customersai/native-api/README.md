# Customers.ai: Native API Reference

A consolidated summary of Customers.ai's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://customers.ai/help/l/en/category/doq3ewxla3-public-api
- **OpenAPI specification:** https://api.mobilemonkey.com/apidocs_public
- **API base URL:** `https://api.mobilemonkey.com/public`

## Authentication

### API Key

Connect with your Customers.ai API key from Integrations > Zapier.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://customers.ai/help/l/en/article/xz9zrxifz3-zapier)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://customers.ai/help/l/en/category/doq3ewxla3-public-api) |
| [List Contact IDs](actions/list-contact-ids.md) | `GET /contacts/ids` | [docs](https://customers.ai/help/l/en/category/doq3ewxla3-public-api) |
| [List Promoters](actions/list-promoters.md) | `GET /promoters` | [docs](https://customers.ai/help/l/en/category/doq3ewxla3-public-api) |
| [Opt-In SMS Contact](actions/opt-in-sms-contact.md) | `PUT /promoters/:id/optin_sms_contact` | [docs](https://customers.ai/help/l/en/category/doq3ewxla3-public-api) |
| [Send Dialogue](actions/send-dialogue.md) | `POST /contacts/:recipient_id/send_dialogue` | [docs](https://customers.ai/help/l/en/category/doq3ewxla3-public-api) |
| [Send JSON Message](actions/send-json-message.md) | `POST /contacts/:recipient_id/send_json_message` | [docs](https://customers.ai/help/l/en/article/8f3i58rfxc-send-json-message) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:recipient_id` | [docs](https://customers.ai/help/l/en/article/4xafzjcgyr-update-contact-attributes-via-api) |
