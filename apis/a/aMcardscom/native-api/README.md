# AMcards.com: Native API Reference

A consolidated summary of AMcards.com's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://staging.amcards.com/docs/
- **API base URL:** `https://amcards.com/.api/v1`

## Authentication

### Access Token

Connect with an AMcards access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://staging.amcards.com/docs/developers-only/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contact/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Create Group](actions/create-group.md) | `POST /group/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/:contactId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Delete Group](actions/delete-group.md) | `DELETE /group/:groupId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaign/:campaignId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Get Card](actions/get-card.md) | `GET /card/:cardId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Get Card Template Category](actions/get-card-template-category.md) | `GET /category/:categoryId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Get Contact](actions/get-contact.md) | `GET /contact/:contactId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Get Group](actions/get-group.md) | `GET /group/:groupId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Get Mailing](actions/get-mailing.md) | `GET /mailing/:mailingId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Get User](actions/get-user.md) | `GET /user/:userId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaign/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Card Template Categories](actions/list-card-template-categories.md) | `GET /category/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Cards](actions/list-cards.md) | `GET /card/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Contacts](actions/list-contacts.md) | `GET /contact/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Groups](actions/list-groups.md) | `GET /group/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Mailings](actions/list-mailings.md) | `GET /mailing/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Public Templates](actions/list-public-templates.md) | `GET /publictemplate/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Quicksend Templates](actions/list-quicksend-templates.md) | `GET /quicksendtemplate/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Templates](actions/list-templates.md) | `GET /template/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [List Users](actions/list-users.md) | `GET /user/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Search Contacts](actions/search-contacts.md) | `GET /contact/search/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Update Contact](actions/update-contact.md) | `PATCH /contact/:contactId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
| [Update Group](actions/update-group.md) | `PATCH /group/:groupId/` | [docs](https://staging.amcards.com/docs/developers-only/) |
