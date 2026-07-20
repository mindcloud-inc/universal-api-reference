# Smoove: Native API Reference

A consolidated summary of Smoove's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://rest.smoove.io
- **OpenAPI specification:** https://rest.smoove.io/swagger/docs/v1
- **API base URL:** `https://rest.smoove.io`

## Authentication

### API Key

Use a Smoove API key as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://skb.smoove.io/en/creating-api-key/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `itemsPerPage` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Contact Exists](actions/check-contact-exists.md) | `GET /v1/Contacts/:id/Exists` | [docs](https://rest.smoove.io) |
| [Create Campaign](actions/create-campaign.md) | `POST /v1/Campaigns` | [docs](https://rest.smoove.io) |
| [Create List](actions/create-list.md) | `POST /v1/Lists` | [docs](https://rest.smoove.io) |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /v1/Contacts` | [docs](https://rest.smoove.io) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /v1/Campaigns/:id` | [docs](https://rest.smoove.io) |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | `GET /v1/Campaigns/:id/Statistics` | [docs](https://rest.smoove.io) |
| [Get Contact](actions/get-contact.md) | `GET /v1/Contacts/:id` | [docs](https://rest.smoove.io) |
| [Get Landing Page](actions/get-landing-page.md) | `GET /v1/LandingPages/:id` | [docs](https://rest.smoove.io) |
| [Get List](actions/get-list.md) | `GET /v1/Lists/:id` | [docs](https://rest.smoove.io) |
| [Import Contacts in Bulk](actions/import-contacts-in-bulk.md) | `POST /v1/Contacts_BulkImport` | [docs](https://rest.smoove.io) |
| [List Active Contacts](actions/list-active-contacts.md) | `GET /v1/Contacts` | [docs](https://rest.smoove.io) |
| [List Blacklisted Contacts](actions/list-blacklisted-contacts.md) | `GET /v1/Contacts_Blacklisted` | [docs](https://rest.smoove.io) |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | `GET /v1/Campaigns/:id/Recipients` | [docs](https://rest.smoove.io) |
| [List Contact Fields](actions/list-contact-fields.md) | `GET /v1/Account/ContactFields` | [docs](https://rest.smoove.io) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /v1/Lists` | [docs](https://rest.smoove.io) |
| [List Contacts In List](actions/list-contacts-in-list.md) | `GET /v1/Lists/:id/Contacts` | [docs](https://rest.smoove.io) |
| [List Landing Page Recipients](actions/list-landing-page-recipients.md) | `GET /v1/LandingPages/:id/Recipients` | [docs](https://rest.smoove.io) |
| [List Landing Pages](actions/list-landing-pages.md) | `GET /v1/LandingPages` | [docs](https://rest.smoove.io) |
| [List Unsubscribed Contacts](actions/list-unsubscribed-contacts.md) | `GET /v1/Contacts_Unsubscribers` | [docs](https://rest.smoove.io) |
| [Resubscribe Contact](actions/resubscribe-contact.md) | `POST /v1/Contacts/:id/Resubscribe` | [docs](https://rest.smoove.io) |
| [Send Campaign](actions/send-campaign.md) | `POST /v1/Campaigns/:id/Send` | [docs](https://rest.smoove.io) |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | `POST /v1/Contacts/:id/Unsubscribe` | [docs](https://rest.smoove.io) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/Contacts/:id` | [docs](https://rest.smoove.io) |
