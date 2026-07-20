# Guestmeter: Native API Reference

A consolidated summary of Guestmeter's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.guestmeter.com/docs/api
- **API base URL:** `https://www.guestmeter.com/api`

## Authentication

### API Key + Secret Key

Authenticate requests using Guestmeter apiKey and secretKey headers.

### Credentials

- **API Key:** `apiKey` · required
- **Secret Key:** `secretKey` · required · Guestmeter `secretKey` header value from Channels > Integration.

Send these headers with each API request:

```http
apiKey: <apiKey>
secretKey: <secretKey>
```

[Official authentication documentation](https://www.guestmeter.com/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Guest](actions/get-guest.md) | `GET /getGuest` | [docs](https://www.guestmeter.com/docs/api#get-guests) |
| [List Guests](actions/list-guests.md) | `GET /getGuestList` | [docs](https://www.guestmeter.com/docs/api#get-ratings) |
| [Send Survey](actions/send-survey.md) | `POST /sendSurvey` | [docs](https://www.guestmeter.com/docs/api#add-guest) |
