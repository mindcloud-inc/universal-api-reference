# updown.io: Native API Reference

A consolidated summary of updown.io's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://updown.io/api
- **API base URL:** `https://updown.io/api`

## Authentication

### API Key

Authenticate with an updown.io API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://updown.io/api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Check](actions/create-check.md) | `POST /checks` | [docs](https://updown.io/api#POST-/api/checks) |
| [Create Recipient](actions/create-recipient.md) | `POST /recipients` | [docs](https://updown.io/api#POST-/api/recipients) |
| [Create Status Page](actions/create-status-page.md) | `POST /status_pages` | [docs](https://updown.io/api#POST-/api/status-pages) |
| [Delete Check](actions/delete-check.md) | `DELETE /checks/:token` | [docs](https://updown.io/api#DELETE-/api/checks/:token) |
| [Delete Recipient](actions/delete-recipient.md) | `DELETE /recipients/:id` | [docs](https://updown.io/api#DELETE-/api/recipients/:id) |
| [Delete Status Page](actions/delete-status-page.md) | `DELETE /status_pages/:token` | [docs](https://updown.io/api#DELETE-/api/status-pages/:token) |
| [Get Check](actions/get-check.md) | `GET /checks/:token` | [docs](https://updown.io/api#GET-/api/checks/:token) |
| [Get Check Metrics](actions/get-check-metrics.md) | `GET /checks/:token/metrics` | [docs](https://updown.io/api#GET-/api/checks/:token/metrics) |
| [List Check Downtimes](actions/list-check-downtimes.md) | `GET /checks/:token/downtimes` | [docs](https://updown.io/api#GET-/api/checks/:token/downtimes) |
| [List Checks](actions/list-checks.md) | `GET /checks` | [docs](https://updown.io/api#GET-/api/checks) |
| [List Node IP Addresses](actions/list-node-ip-addresses.md) | `GET /nodes/ips` | [docs](https://updown.io/api#GET-/api/nodes/ips) |
| [List Node IPv4 Addresses](actions/list-node-ipv4-addresses.md) | `GET /nodes/ipv4` | [docs](https://updown.io/api#GET-/api/nodes/ipv4) |
| [List Node IPv6 Addresses](actions/list-node-ipv6-addresses.md) | `GET /nodes/ipv6` | [docs](https://updown.io/api#GET-/api/nodes/ipv6) |
| [List Nodes](actions/list-nodes.md) | `GET /nodes` | [docs](https://updown.io/api#GET-/api/nodes) |
| [List Recipients](actions/list-recipients.md) | `GET /recipients` | [docs](https://updown.io/api#GET-/api/recipients) |
| [List Status Pages](actions/list-status-pages.md) | `GET /status_pages` | [docs](https://updown.io/api#GET-/api/status-pages) |
| [Update Check](actions/update-check.md) | `PUT /checks/:token` | [docs](https://updown.io/api#PUT-/api/checks/:token) |
| [Update Status Page](actions/update-status-page.md) | `PUT /status_pages/:token` | [docs](https://updown.io/api#PUT-/api/status-pages/:token) |
