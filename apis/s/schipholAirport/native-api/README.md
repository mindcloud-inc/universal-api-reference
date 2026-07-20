# Schiphol Airport: Native API Reference

A consolidated summary of Schiphol Airport's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developer.schiphol.nl/apis/flight-api/v4/quickstarts
- **API base URL:** `https://api.schiphol.nl/public-flights`

## Authentication

### App ID and Key

Authenticate to the Schiphol Public Flight API with the developer portal app_id and app_key headers.

### Credentials

- **App ID:** `appId` · required · Schiphol developer portal application ID.
- **App Key:** `appKey` · required · Schiphol developer portal application key.

[Official authentication documentation](https://developer.schiphol.nl/apis/flight-api/v4/quickstarts)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `+` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Airline](actions/get-airline.md) | `GET /airlines/:airline` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights/get) |
| [Get Destination](actions/get-destination.md) | `GET /destinations/:iata` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/destinations-iata/get) |
| [Get Flight](actions/get-flight.md) | `GET /flights/:id` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights-id/get) |
| [List Aircraft Types](actions/list-aircraft-types.md) | `GET /aircrafttypes` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/aircrafttypes/get) |
| [List Airlines](actions/list-airlines.md) | `GET /airlines` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights/get) |
| [List Destinations](actions/list-destinations.md) | `GET /destinations` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/destinations/get) |
| [List Flight IDs](actions/list-flight-ids.md) | `GET /flights/ids` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights-id/get) |
| [List Flights](actions/list-flights.md) | `GET /flights` | [docs](https://developer-dev.internal.schiphol.nl/apis/public-flight/versions/469ffd39-f601-4ba0-855e-f6a6e5f427b7/paths/flights/get) |
