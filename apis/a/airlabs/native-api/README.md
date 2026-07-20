# Airlabs: Native API Reference

A consolidated summary of Airlabs's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://airlabs.co/docs/
- **API base URL:** `https://airlabs.co/api/v9`

## Authentication

### API Key

Authenticate with an AirLabs API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://airlabs.co/docs/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Flight Alert Listener](actions/create-flight-alert-listener.md) | `GET /listen` | [docs](https://airlabs.co/docs/alert) |
| [Delete Flight Alert Listener](actions/delete-flight-alert-listener.md) | `GET /unlisten` | [docs](https://airlabs.co/docs/alert) |
| [Find Nearby Airports](actions/find-nearby-airports.md) | `GET /nearby` | [docs](https://airlabs.co/docs/nearby) |
| [Get Flight Information](actions/get-flight-information.md) | `GET /flight` | [docs](https://airlabs.co/docs/flight) |
| [List Aircraft Fleets](actions/list-aircraft-fleets.md) | `GET /fleets` | [docs](https://airlabs.co/docs/fleets) |
| [List Airlines](actions/list-airlines.md) | `GET /airlines` | [docs](https://airlabs.co/docs/airlines) |
| [List Airports](actions/list-airports.md) | `GET /airports` | [docs](https://airlabs.co/docs/airports) |
| [List Cities](actions/list-cities.md) | `GET /cities` | [docs](https://airlabs.co/docs/cities) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://airlabs.co/docs/countries) |
| [List Flight Alert Listeners](actions/list-flight-alert-listeners.md) | `GET /listeners` | [docs](https://airlabs.co/docs/alert) |
| [List Flight Alert Webhook History](actions/list-flight-alert-webhook-history.md) | `GET /webhooks` | [docs](https://airlabs.co/docs/alert) |
| [List Flight Schedules](actions/list-flight-schedules.md) | `GET /schedules` | [docs](https://airlabs.co/docs/schedules) |
| [List Real-Time Flights](actions/list-real-time-flights.md) | `GET /flights` | [docs](https://airlabs.co/docs/flights) |
| [List Routes](actions/list-routes.md) | `GET /routes` | [docs](https://airlabs.co/docs/routes) |
| [List Tax Codes](actions/list-tax-codes.md) | `GET /taxes` | [docs](https://airlabs.co/docs/taxes) |
| [List Time Zones](actions/list-time-zones.md) | `GET /timezones` | [docs](https://airlabs.co/docs/timezones) |
| [Ping Airlabs](actions/ping-airlabs.md) | `GET /ping` | [docs](https://airlabs.co/docs/) |
| [Suggest Destinations](actions/suggest-destinations.md) | `GET /suggest` | [docs](https://airlabs.co/docs/suggest) |
