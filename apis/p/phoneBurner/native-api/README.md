# PhoneBurner: Native API Reference

A consolidated summary of PhoneBurner's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.phoneburner.com/developer/route_list
- **API base URL:** `https://www.phoneburner.com/`

## Authentication

### Personal Access Token

PhoneBurner Personal Access Token used as a bearer token for API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.phoneburner.com/hc/en-us/articles/36826752283028-Generate-a-Personal-Access-Token-PAT)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST rest/1/contacts` | [docs](https://www.phoneburner.com/developer/route_list#contacts) |
| [Delete Contact](actions/delete-contact.md) | `DELETE rest/1/contacts/{{contactId}}` | [docs](https://www.phoneburner.com/developer/route_list#contacts) |
| [List Contacts](actions/list-contacts.md) | `GET rest/1/contacts` | [docs](https://www.phoneburner.com/developer/route_list#contacts) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET rest/1/contacts/{{contactId}}` | [docs](https://www.phoneburner.com/developer/route_list#contacts) |
| [Update Contact](actions/update-contact.md) | `PUT rest/1/contacts/{{contactId}}` | [docs](https://www.phoneburner.com/developer/route_list#contacts) |
