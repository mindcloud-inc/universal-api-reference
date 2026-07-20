# Joonto: Native API Reference

A consolidated summary of Joonto's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://api.joonto.com/docs/index.html
- **OpenAPI specification:** https://api.joonto.com/swagger/v1/swagger.json
- **API base URL:** `https://api.joonto.com`

## Authentication

### API Token

Use an existing Joonto dashboard API token for bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.joonto.com/docs/index.html)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Avatar Image By Contact](actions/get-avatar-image-by-contact.md) | `GET /api/Images/GetByContact` | [docs](https://api.joonto.com/docs/index.html) |
| [Get Avatar Image By User Email](actions/get-avatar-image-by-user-email.md) | `GET /api/Images/GetByUserEmail` | [docs](https://api.joonto.com/docs/index.html) |
| [Get Call Details](actions/get-call-details.md) | `GET /api/Calls/Get/:id` | [docs](https://api.joonto.com/docs/index.html) |
| [Get Caller Name](actions/get-caller-name.md) | `GET /api/Calls/GetCallerName` | [docs](https://api.joonto.com/docs/index.html) |
| [Get Calls Leaderboard](actions/get-calls-leaderboard.md) | `POST /api/Live/Leaderboard/:filter` | [docs](https://api.joonto.com/docs/index.html) |
| [Get Current User](actions/get-current-user.md) | `GET /api/Users/me` | [docs](https://api.joonto.com/docs/index.html) |
| [Get Dashboard Call Summary](actions/get-dashboard-call-summary.md) | `POST /api/Dashboard/CallSummary/:filter` | [docs](https://api.joonto.com/docs/index.html) |
| [Get SMS By User And Phone Number](actions/get-sms-by-user-and-phone-number.md) | `GET /api/SMS/GetByUserAndPhoneNumber` | [docs](https://api.joonto.com/docs/index.html) |
| [Get SMS Details](actions/get-sms-details.md) | `GET /api/SMS/Get/:id` | [docs](https://api.joonto.com/docs/index.html) |
| [Get User Details](actions/get-user-details.md) | `GET /api/Users/Get/:id` | [docs](https://api.joonto.com/docs/index.html) |
| [List Live Calls](actions/list-live-calls.md) | `POST /api/Live/Calls/:filter` | [docs](https://api.joonto.com/docs/index.html) |
| [List New SMS By User](actions/list-new-sms-by-user.md) | `POST /api/Users/GetNewSmsByUser` | [docs](https://api.joonto.com/docs/index.html) |
| [List SMS Contacts](actions/list-sms-contacts.md) | `POST /api/Users/GetSmsContacts` | [docs](https://api.joonto.com/docs/index.html) |
