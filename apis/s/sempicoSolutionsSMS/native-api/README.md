# Sempico Solutions SMS: Native API Reference

A consolidated summary of Sempico Solutions SMS's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://restapi.gatum.io/desc/
- **API base URL:** `https://restapi.sempico.solutions/v1`

## Authentication

### API Token

Authenticate Sempico REST API requests with the access token in the X-Access-Token header.

### Credentials

- **Access token:** `apiKey` · required

Send these headers with each API request:

```http
X-Access-Token: <apiKey>
```

[Official authentication documentation](https://restapi.gatum.io/desc/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Numbers to Blacklist](actions/add-numbers-to-blacklist.md) | `POST /black-list-add` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Add Numbers to Group](actions/add-numbers-to-group.md) | `POST /group-number-add` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Create Group](actions/create-group.md) | `POST /group-create` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Delete Blacklist Numbers](actions/delete-blacklist-numbers.md) | `POST /black-list-delete` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Delete Group Numbers](actions/delete-group-numbers.md) | `POST /group-number-delete` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Delete Groups](actions/delete-groups.md) | `POST /group-delete` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Get Account Information](actions/get-account-information.md) | `GET /me` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [List Groups](actions/list-groups.md) | `POST /group` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Search Group Numbers](actions/search-group-numbers.md) | `POST /group-number-search` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Search Sent SMS](actions/search-sent-sms.md) | `POST /sms-full-data` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /send-bulk` | [docs](https://pypi.org/pypi/gatum-rest-py/json) |
| [Send SMS](actions/send-sms.md) | `POST /send` | [docs](https://restapi.gatum.io/desc/) |
