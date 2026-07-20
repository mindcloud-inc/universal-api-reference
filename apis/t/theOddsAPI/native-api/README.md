# The Odds: Native API Reference

A consolidated summary of The Odds's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://the-odds-api.com/liveapi/guides/v4/
- **API base URL:** `https://api.the-odds-api.com`

## Authentication

### API Key Query Auth

Authenticates requests by sending the tenant API key as query parameter apiKey on every request.

### Credentials

- **API Key:** `apiKey` · required · Your The Odds API key. This value is sent as the apiKey query parameter on every request.

[Official authentication documentation](https://the-odds-api.com/liveapi/guides/v4/)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Event Markets](actions/get-event-markets.md) | `GET /v4/sports/:sport/events/:eventId/markets` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-event-markets) |
| [Get Event Odds](actions/get-event-odds.md) | `GET /v4/sports/:sport/events/:eventId/odds` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-event-odds) |
| [Get Historical Event Odds](actions/get-historical-event-odds.md) | `GET /v4/historical/sports/:sport/events/:eventId/odds` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-historical-event-odds) |
| [List Events](actions/list-events.md) | `GET /v4/sports/:sport/events` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-events) |
| [List Historical Events](actions/list-historical-events.md) | `GET /v4/historical/sports/:sport/events` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-historical-events) |
| [List Historical Odds](actions/list-historical-odds.md) | `GET /v4/historical/sports/:sport/odds` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-historical-odds) |
| [List Odds](actions/list-odds.md) | `GET /v4/sports/:sport/odds/` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-odds) |
| [List Participants](actions/list-participants.md) | `GET /v4/sports/:sport/participants` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-participants) |
| [List Scores](actions/list-scores.md) | `GET /v4/sports/:sport/scores/` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-scores) |
| [List Sports](actions/list-sports.md) | `GET /v4/sports/` | [docs](https://the-odds-api.com/liveapi/guides/v4/#get-sports) |
