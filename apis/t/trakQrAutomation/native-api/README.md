# Trak Qr Automation: Native API Reference

A consolidated summary of Trak Qr Automation's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link
- **API base URL:** `https://backend.trak.codes/api/v0`

## Authentication

### API Key

Authenticate Trak Events Partner API requests with the API key in the X-API-KEY HTTP header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Attendee](actions/create-attendee.md) | `POST /events/:eventKey/attendees` | [docs](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link) |
| [Create Partner](actions/create-partner.md) | `POST /events-partners` | [docs](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link) |
| [Get Partner Balance](actions/get-partner-balance.md) | `GET /events-partners/balance` | [docs](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link) |
