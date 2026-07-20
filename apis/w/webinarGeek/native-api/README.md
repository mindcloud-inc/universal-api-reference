# WebinarGeek: Native API Reference

A consolidated summary of WebinarGeek's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://webinargeek.docs.apiary.io/
- **API base URL:** `https://app.webinargeek.com/api/v2`

## Authentication

### API Key

Connect WebinarGeek with an API key from your account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Api-Token: <apiKey>
```

[Official authentication documentation](https://static.webinargeek.com/api-documentation.html#header-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Set the direction separately with `sort`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Broadcasts](actions/list-broadcasts.md) | `GET /broadcasts` | [docs](https://static.webinargeek.com/api-documentation.html#broadcasts-get) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://static.webinargeek.com/api-documentation.html#messages-get) |
| [List Questions](actions/list-questions.md) | `GET /questions` | [docs](https://static.webinargeek.com/api-documentation.html#questions-get) |
| [List Subscription Payments](actions/list-subscription-payments.md) | `GET /subscription_payments` | [docs](https://static.webinargeek.com/api-documentation.html#subscription-payments-get) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://static.webinargeek.com/api-documentation.html#subscriptions-get) |
| [List Webinars](actions/list-webinars.md) | `GET /webinars` | [docs](https://static.webinargeek.com/api-documentation.html#webinars-get) |
| [Retrieve Account Metadata](actions/retrieve-account-metadata.md) | `GET /account` | [docs](https://static.webinargeek.com/api-documentation.html#account-get) |
| [Retrieve Broadcast](actions/retrieve-broadcast.md) | `GET /broadcasts/:broadcastId` | [docs](https://static.webinargeek.com/api-documentation.html#broadcasts-get-1) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET /subscriptions/:subscriptionId` | [docs](https://static.webinargeek.com/api-documentation.html#subscriptions-get-1) |
| [Retrieve Webinar](actions/retrieve-webinar.md) | `GET /webinars/:webinarId` | [docs](https://static.webinargeek.com/api-documentation.html#webinars-get-1) |
| [Subscribe to Broadcast](actions/subscribe-to-broadcast.md) | `POST /broadcasts/:broadcastId/subscriptions` | [docs](https://static.webinargeek.com/api-documentation.html) |
