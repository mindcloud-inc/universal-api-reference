# EchtPost Postcards: Native API Reference

A consolidated summary of EchtPost Postcards's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle
- **OpenAPI specification:** https://api.echtpost.de/api-docs/v1/swagger.json
- **API base URL:** `https://api.echtpost.de/v1`

## Authentication

### API Key

Use an EchtPost API key created in the EchtPost account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-apikey: <apiKey>
```

[Official authentication documentation](https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Credits](actions/add-credits.md) | `POST /credits` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [Create Card From Contact](actions/create-card-from-contact.md) | `POST /cards` | [docs](https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle) |
| [Create Card From Contact Data](actions/create-card-from-contact-data.md) | `POST /cards` | [docs](https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle) |
| [Create Card From Contact Group](actions/create-card-from-contact-group.md) | `POST /cards` | [docs](https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle) |
| [Create Card From Contact List](actions/create-card-from-contact-list.md) | `POST /cards` | [docs](https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle) |
| [Delete Card](actions/delete-card.md) | `DELETE /cards/:id` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [Get Card](actions/get-card.md) | `GET /cards/:id` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [List Cards](actions/list-cards.md) | `GET /cards` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.echtpost.de/api-docs/index.html) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://api.echtpost.de/api-docs/index.html) |
