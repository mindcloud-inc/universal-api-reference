# BKK Futar: Native API Reference

A consolidated summary of BKK Futar's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://bkkfutar.docs.apiary.io/
- **API base URL:** `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`

## Authentication

### API Key

BKK Futar API key used as the query parameter key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://opendata.bkk.hu/data-sources)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Arrivals And Departures For Stop](actions/get-arrivals-and-departures-for-stop.md) | `GET /arrivals-and-departures-for-stop.json` | [docs](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-arrivals-and-departures-for-stop) |
| [Get Bicycle Rental Stations](actions/get-bicycle-rental-stations.md) | `GET /bicycle-rental.json` | [docs](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-bicycle-rental-stations) |
| [Get References](actions/get-references.md) | `GET /references.json` | [docs](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-references) |
| [Get Schedule For Stop](actions/get-schedule-for-stop.md) | `GET /schedule-for-stop.json` | [docs](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-schedule-for-stop) |
| [Get Stops For Location](actions/get-stops-for-location.md) | `GET /stops-for-location.json` | [docs](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-stops-for-location) |
| [Get Vehicles For Stop](actions/get-vehicles-for-stop.md) | `GET /vehicles-for-stop.json` | [docs](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#get-vehicles-for-stop) |
| [Search Alerts](actions/search-alerts.md) | `GET /search.json` | [docs](https://learn.microsoft.com/en-us/connectors/bkkfutarip/#search-alerts) |
