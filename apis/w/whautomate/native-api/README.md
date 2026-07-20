# Whautomate: Native API Reference

A consolidated summary of Whautomate's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://help.whautomate.com/product-guides/whautomate-rest-api
- **API base URL:** `https://api.whautomate.com`

## Authentication

### API Key

Connect with a Whautomate REST API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://help.whautomate.com/product-guides/whautomate-rest-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Client](actions/add-client.md) | `POST /v1/clients` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/clients) |
| [Add Client Tag](actions/add-client-tag.md) | `POST /v1/clientTags` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/client-tags) |
| [Add Contact](actions/add-contact.md) | `POST /v1/contacts` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts) |
| [Add Tags to Client](actions/add-tags-to-client.md) | `POST /v1/clients/{{clientId}}/tags/add` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/clients) |
| [Delete Client](actions/delete-client.md) | `DELETE /v1/clients/{{clientId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/clients) |
| [Delete Client Tag](actions/delete-client-tag.md) | `DELETE /v1/clientTags/{{clientTagId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/client-tags) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contacts/{{contactId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts) |
| [Get Account Info](actions/get-account-info.md) | `GET /v1/account-info` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api) |
| [Get Client](actions/get-client.md) | `GET /v1/clients/{{clientId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/clients) |
| [Get Client Tag](actions/get-client-tag.md) | `GET /v1/clientTags/{{clientTagId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/client-tags) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/{{contactId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts) |
| [Get Location](actions/get-location.md) | `GET /v1/locations/{{locationId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/locations) |
| [Get Staff](actions/get-staff.md) | `GET /v1/staffs/{{staffId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/staffs) |
| [List Client Tags](actions/list-client-tags.md) | `GET /v1/clientTags` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/client-tags) |
| [List Locations](actions/list-locations.md) | `GET /v1/locations` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/locations) |
| [List Staffs](actions/list-staffs.md) | `GET /v1/staffs` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/staffs) |
| [Remove Tags from Client](actions/remove-tags-from-client.md) | `POST /v1/clients/{{clientId}}/tags/remove` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/clients) |
| [Search Clients](actions/search-clients.md) | `GET /v1/clients` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/clients) |
| [Search Contacts](actions/search-contacts.md) | `GET /v1/contacts` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts) |
| [Update Client](actions/update-client.md) | `PUT /v1/clients/{{clientId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/clients) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/contacts/{{contactId}}` | [docs](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts) |
