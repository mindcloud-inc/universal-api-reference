# WEEEK: Native API Reference

A consolidated summary of WEEEK's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://developers.weeek.net/
- **API base URL:** `https://api.weeek.net/public/v1`

## Authentication

### Access Token

Use a WEEEK workspace access token. MindCloud sends it as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.weeek.net/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /crm/contacts` | [docs](https://developers.weeek.net/api) |
| [Create Organization](actions/create-organization.md) | `POST /crm/organizations` | [docs](https://developers.weeek.net/api) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /crm/contacts/:contactId` | [docs](https://developers.weeek.net/api) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /crm/organizations/:organizationId` | [docs](https://developers.weeek.net/api) |
| [Get Contact](actions/get-contact.md) | `GET /crm/contacts/:contactId` | [docs](https://developers.weeek.net/api) |
| [Get Organization](actions/get-organization.md) | `GET /crm/organizations/:organizationId` | [docs](https://developers.weeek.net/api) |
| [List Contacts](actions/list-contacts.md) | `GET /crm/contacts` | [docs](https://developers.weeek.net/api) |
| [List Organizations](actions/list-organizations.md) | `GET /crm/organizations` | [docs](https://developers.weeek.net/api) |
| [Update Contact](actions/update-contact.md) | `PATCH /crm/contacts/:contactId` | [docs](https://developers.weeek.net/api) |
| [Update Organization](actions/update-organization.md) | `PATCH /crm/organizations/:organizationId` | [docs](https://developers.weeek.net/api) |
