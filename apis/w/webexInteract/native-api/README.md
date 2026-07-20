# Webex Interact: Native API Reference

A consolidated summary of Webex Interact's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.webexinteract.com/reference/webex-interact-api-introduction
- **API base URL:** `https://api.webexinteract.com`

## Authentication

### Webex Interact API key

Authenticates Webex Interact requests by sending the API project access token in the X-AUTH-KEY request header.

### Credentials

- **API key:** `apiKey` · required · Webex Interact API project access token. Runtime sends this value in the X-AUTH-KEY header.

Send these headers with each API request:

```http
X-AUTH-KEY: <apiKey>
```

[Official authentication documentation](https://docs.webexinteract.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`. The total page count is read from `paging.total_pages`. The current page number is read from `paging.current_page`.

## Pagination

Use `page_size` in the query string to set the page size (default 25; accepted range 1–100). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_order`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel scheduled SMS request](actions/cancel-scheduled-sms-request.md) | `DELETE /campaigns/v1/cancel/{id}` | [docs](https://docs.webexinteract.com/reference/scheduled-messages-api) |
| [Create contact list](actions/create-contact-list.md) | `POST /contacts/v1/lists/create` | [docs](https://docs.webexinteract.com/reference/lists-api) |
| [Create or update contacts](actions/create-or-update-contacts.md) | `POST /contacts/v1/contacts` | [docs](https://docs.webexinteract.com/reference/contacts-api) |
| [Create shortlink](actions/create-shortlink.md) | `POST /assets/v1/shortlink` | [docs](https://docs.webexinteract.com/reference/shortlinks-api) |
| [Delete contact](actions/delete-contact.md) | `DELETE /contacts/v1/contacts/{contactId}` | [docs](https://docs.webexinteract.com/reference/contacts-api) |
| [Delete contact list](actions/delete-contact-list.md) | `DELETE /contacts/v1/lists/{uid}` | [docs](https://docs.webexinteract.com/reference/lists-api) |
| [Delete sender](actions/delete-sender.md) | `DELETE /assets/v1/senders/{id}` | [docs](https://docs.webexinteract.com/reference/senders-api) |
| [Delete shortlink](actions/delete-shortlink.md) | `DELETE /assets/v1/shortlink/{linkId}` | [docs](https://docs.webexinteract.com/reference/shortlinks-api) |
| [Filter shortlinks](actions/filter-shortlinks.md) | `POST /assets/v1/shortlink/filter` | [docs](https://docs.webexinteract.com/reference/shortlinks-api) |
| [List contact lists](actions/list-contact-lists.md) | `GET /contacts/v1/lists` | [docs](https://docs.webexinteract.com/reference/lists-api) |
| [List contacts in list](actions/list-contacts-in-list.md) | `GET /contacts/v1/contacts/list/{listId}` | [docs](https://docs.webexinteract.com/reference/contacts-api) |
| [List scheduled SMS by created date range](actions/list-scheduled-sms-by-created-date-range.md) | `POST /campaigns/v1/scheduled` | [docs](https://docs.webexinteract.com/reference/scheduled-messages-api) |
| [List scheduled SMS by scheduled date range](actions/list-scheduled-sms-by-scheduled-date-range.md) | `POST /campaigns/v1/scheduled` | [docs](https://docs.webexinteract.com/reference/scheduled-messages-api) |
| [List senders](actions/list-senders.md) | `GET /assets/v1/senders` | [docs](https://docs.webexinteract.com/reference/senders-api) |
| [Retrieve account metadata](actions/retrieve-account-metadata.md) | `GET /identity/v1/account` | [docs](https://docs.webexinteract.com/reference/account-api) |
| [Retrieve scheduled SMS request](actions/retrieve-scheduled-sms-request.md) | `POST /campaigns/v1/scheduled` | [docs](https://docs.webexinteract.com/reference/scheduled-messages-api) |
| [Retrieve sender](actions/retrieve-sender.md) | `GET /assets/v1/senders/{id}` | [docs](https://docs.webexinteract.com/reference/senders-api) |
| [Retrieve shortlink](actions/retrieve-shortlink.md) | `GET /assets/v1/shortlink/{linkId}` | [docs](https://docs.webexinteract.com/reference/shortlinks-api) |
| [Send template SMS](actions/send-template-sms.md) | `POST /v1/sms` | [docs](https://docs.webexinteract.com/reference/sms-api) |
| [Send text SMS](actions/send-text-sms.md) | `POST /v1/sms` | [docs](https://docs.webexinteract.com/reference/sms-api) |
| [Test template SMS](actions/test-template-sms.md) | `POST /v1/sms/test` | [docs](https://docs.webexinteract.com/reference/sms-api) |
| [Test text SMS](actions/test-text-sms.md) | `POST /v1/sms/test` | [docs](https://docs.webexinteract.com/reference/sms-api) |
