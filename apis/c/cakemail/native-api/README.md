# Cakemail: Native API Reference

A consolidated summary of Cakemail's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://cakemail.dev/api
- **OpenAPI specification:** https://cakemail.dev/en/assets/api-openapi.yaml-8BCXY7vV.js
- **API base URL:** `https://api.cakemail.dev`

## Authentication

### Bearer Token

Cakemail API access token used as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://cakemail.dev/api/guides/getting-started-ng-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `pagination.next_cursor`.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | `POST /lists/:listId/contacts` | [docs](https://cakemail.dev/en/api/contact#add-a-contact) |
| [Archive List](actions/archive-list.md) | `POST /lists/:listId/archive` | [docs](https://cakemail.dev/en/api/list#archive-a-list) |
| [Create Contact Tag](actions/create-contact-tag.md) | `POST /tags` | [docs](https://cakemail.dev/en/api/tags#create-a-contact-tag) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://cakemail.dev/en/api/list#create-a-list) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /lists/:listId/contacts/:contactId` | [docs](https://cakemail.dev/en/api/contact#delete-a-contact) |
| [Delete Contact Tag](actions/delete-contact-tag.md) | `DELETE /tags/:tag` | [docs](https://cakemail.dev/en/api/tags#delete-a-contact-tag) |
| [Edit Contact Tag](actions/edit-contact-tag.md) | `PATCH /tags/:tag` | [docs](https://cakemail.dev/en/api/tags#edit-a-contact-tag) |
| [Get Account Details](actions/get-account-details.md) | `GET /accounts/self` | [docs](https://cakemail.dev/en/api/account#show-my-account-details) |
| [Get Contact](actions/get-contact.md) | `GET /lists/:listId/contacts/:contactId` | [docs](https://cakemail.dev/en/api/contact#show-a-contact-details) |
| [Get List](actions/get-list.md) | `GET /lists/:listId` | [docs](https://cakemail.dev/en/api/list#show-a-list-parameters) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://cakemail.dev/en/api/campaign#show-all-campaigns) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /tags` | [docs](https://cakemail.dev/en/api/tags#list-contact-tags) |
| [List Contacts](actions/list-contacts.md) | `GET /lists/:listId/contacts` | [docs](https://cakemail.dev/en/api/contact#show-contacts-of-a-list) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://cakemail.dev/en/api/list#show-all-lists) |
| [List Senders](actions/list-senders.md) | `GET /brands/default/senders` | [docs](https://cakemail.dev/en/api/sender#show-all-senders) |
| [Show Contact Tag](actions/show-contact-tag.md) | `GET /tags/:tag` | [docs](https://cakemail.dev/en/api/tags#show-a-contact-tag) |
| [Show Email Activity Logs](actions/show-email-activity-logs.md) | `GET /logs/emails` | [docs](https://cakemail.dev/en/api/log#show-email-activity-logs) |
| [Show My Account Report](actions/show-my-account-report.md) | `GET /reports/accounts/self` | [docs](https://cakemail.dev/en/api/report#show-my-account-report) |
| [Tag Contact](actions/tag-contact.md) | `POST /lists/:listId/contacts/:contactId/tag` | [docs](https://cakemail.dev/en/api/contact#tags-a-contact) |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | `POST /lists/:listId/contacts/:contactId/unsubscribe` | [docs](https://cakemail.dev/en/api/contact#unsubscribe-a-contact-from-a-list) |
| [Untag Contact](actions/untag-contact.md) | `POST /lists/:listId/contacts/:contactId/untag` | [docs](https://cakemail.dev/en/api/contact#untags-a-contact) |
| [Update Contact](actions/update-contact.md) | `PATCH /lists/:listId/contacts/:contactId` | [docs](https://cakemail.dev/en/api/contact#update-a-contact) |
| [Update List](actions/update-list.md) | `PATCH /lists/:listId` | [docs](https://cakemail.dev/en/api/list#update-a-list-parameters) |
| [Validate Domains](actions/validate-domains.md) | `GET /brands/default/domains/default/validate` | [docs](https://cakemail.dev/en/api/domain#validate-domains) |
