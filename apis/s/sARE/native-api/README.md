# SARE: Native API Reference

A consolidated summary of SARE's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://dev.sare.pl/rest-api/other/index.html
- **OpenAPI specification:** https://dev.sare.pl/rest-api/other/swagger.json?version=0.17.2
- **API base URL:** `https://s.enewsletter.pl/api/v1/{uid}`

## Authentication

### API Key

Connect to SARE's current REST API with your account UID and REST API key.

### Credentials

- **API Key:** `apiKey` · required
- **UID:** `uid` · required · Enter the unique SARE account UID that appears in the REST API base URL.

Send these headers with each API request:

```http
ApiKey: <apiKey>
```

[Official authentication documentation](https://dev.sare.pl/rest-api/other/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscribers](actions/add-subscribers.md) | `POST /email/add` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Add Subscribers To Groups By Email Address](actions/add-subscribers-to-groups-by-email-address.md) | `POST /group/add_emails` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Clear Group](actions/clear-group.md) | `POST /group/clear/:group` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Create Group](actions/create-group.md) | `POST /group/add` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Delete Group](actions/delete-group.md) | `POST /group/remove/:group` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Delete Subscribers](actions/delete-subscribers.md) | `POST /email/delete` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Get Group](actions/get-group.md) | `GET /group/get/:group` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Get Subscriber By Email Hash](actions/get-subscriber-by-email-hash.md) | `GET /email/by_email_hash/:emailHash` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Get Subscriber Status By Email Hash](actions/get-subscriber-status-by-email-hash.md) | `GET /email/status_hash/:emailHash` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Get Subscriber Statuses By Email List](actions/get-subscriber-statuses-by-email-list.md) | `POST /email/status_by_email_list/:page` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Get Subscribers By Email List](actions/get-subscribers-by-email-list.md) | `POST /email/by_email_list/:page` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [List Available Group Numbers](actions/list-available-group-numbers.md) | `GET /group/free` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [List Email Properties](actions/list-email-properties.md) | `GET /email/props` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [List Group Emails](actions/list-group-emails.md) | `GET /group/emails/:group/:page` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [List Groups](actions/list-groups.md) | `GET /group/list` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Remove Subscribers From Groups By Email Address](actions/remove-subscribers-from-groups-by-email-address.md) | `POST /group/remove_emails` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Update Group](actions/update-group.md) | `POST /group/edit` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
| [Update Subscribers](actions/update-subscribers.md) | `POST /email/edit` | [docs](https://dev.sare.pl/rest-api/other/index.html) |
