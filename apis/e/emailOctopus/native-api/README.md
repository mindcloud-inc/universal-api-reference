# EmailOctopus: Native API Reference

A consolidated summary of EmailOctopus's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://emailoctopus.com/api-documentation
- **API base URL:** `https://emailoctopus.com/api/1.6`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.emailoctopus.com/article/165-how-to-create-and-delete-api-keys)

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /lists/:listId/contacts` | [docs](https://emailoctopus.com/api-documentation/lists/create-contact) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://emailoctopus.com/api-documentation/lists/create) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /lists/:listId/contacts/:memberId` | [docs](https://emailoctopus.com/api-documentation/lists/delete-contact) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/:listId` | [docs](https://emailoctopus.com/api-documentation/lists/delete) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://emailoctopus.com/api-documentation/campaigns/get) |
| [Get Campaign Report: Bounced](actions/get-campaign-report-bounced.md) | `GET /campaigns/:campaignId/report/bounced` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-bounced) |
| [Get Campaign Report: Clicked](actions/get-campaign-report-clicked.md) | `GET /campaigns/:campaignId/report/clicked` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-clicked) |
| [Get Campaign Report: Links](actions/get-campaign-report-links.md) | `GET /campaigns/:campaignId/report/links` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-links) |
| [Get Campaign Report: Not Clicked](actions/get-campaign-report-not-clicked.md) | `GET /campaigns/:campaignId/report/not-clicked` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-not-clicked) |
| [Get Campaign Report: Opened](actions/get-campaign-report-opened.md) | `GET /campaigns/:campaignId/report/opened` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-opened) |
| [Get Campaign Report: Sent](actions/get-campaign-report-sent.md) | `GET /campaigns/:campaignId/report/sent` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-sent) |
| [Get Campaign Report: Summary](actions/get-campaign-report-summary.md) | `GET /campaigns/:campaignId/report/summary` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-summary) |
| [Get Campaign Report: Unsubscribed](actions/get-campaign-report-unsubscribed.md) | `GET /campaigns/:campaignId/report/unsubscribed` | [docs](https://emailoctopus.com/api-documentation/campaigns/report/get-unsubscribed) |
| [Get Contact](actions/get-contact.md) | `GET /lists/:listId/contacts/:memberId` | [docs](https://emailoctopus.com/api-documentation/lists/get-contact) |
| [Get List](actions/get-list.md) | `GET /lists/:listId` | [docs](https://emailoctopus.com/api-documentation/lists/get) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://emailoctopus.com/api-documentation/campaigns/get-all) |
| [List Contacts](actions/list-contacts.md) | `GET /lists/:listId/contacts` | [docs](https://emailoctopus.com/api-documentation/lists/get-all-contacts) |
| [List Contacts by Tag](actions/list-contacts-by-tag.md) | `GET /lists/:listId/tags/:listTag/contacts` | [docs](https://emailoctopus.com/api-documentation/lists/get-tagged) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://emailoctopus.com/api-documentation/lists/get-all) |
| [List Subscribed Contacts](actions/list-subscribed-contacts.md) | `GET /lists/:listId/contacts/subscribed` | [docs](https://emailoctopus.com/api-documentation/lists/get-subscribed-contacts) |
| [List Unsubscribed Contacts](actions/list-unsubscribed-contacts.md) | `GET /lists/:listId/contacts/unsubscribed` | [docs](https://emailoctopus.com/api-documentation/lists/get-unsubscribed-contacts) |
| [Update Contact](actions/update-contact.md) | `PUT /lists/:listId/contacts/:memberId` | [docs](https://emailoctopus.com/api-documentation/lists/update-contact) |
| [Update List](actions/update-list.md) | `PUT /lists/:listId` | [docs](https://emailoctopus.com/api-documentation/lists/update) |
| [Update Multiple Contacts](actions/update-multiple-contacts.md) | `PUT /lists/:listId/contacts` | [docs](https://emailoctopus.com/api-documentation/lists/update-contact-bulk) |
