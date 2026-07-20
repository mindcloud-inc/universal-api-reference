# Pagerly: Native API Reference

A consolidated summary of Pagerly's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.pagerly.io/api/rotations-endpoint
- **API base URL:** `https://api.pagerly.io/pagerly`

## Authentication

### API Key

Connect with a Pagerly API key passed in the X-APIKEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-APIKEY: <apiKey>
```

[Official authentication documentation](https://docs.pagerly.io/api/rotations-endpoint)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current On-Call Jira Account](actions/get-current-on-call-jira-account.md) | `GET /o/currentusersforjira` | [docs](https://docs.pagerly.io/fetch-current-oncall-rotated-user-via-api) |
| [List Current On-Call Users](actions/list-current-on-call-users.md) | `GET /o/currentusers` | [docs](https://docs.pagerly.io/api/rotations-endpoint) |
| [List Teams](actions/list-teams.md) | `GET /o/zapier/allteams` | [docs](https://docs.pagerly.io/api/rotations-endpoint) |
