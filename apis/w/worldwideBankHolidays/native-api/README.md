# Worldwide Bank Holidays: Native API Reference

A consolidated summary of Worldwide Bank Holidays's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://date.nager.at/API
- **OpenAPI specification:** https://date.nager.at/openapi/v3.json
- **API base URL:** `https://date.nager.at`

## Authentication

### No authentication

Nager.Date v3 public API endpoints are available without authentication.

This API does not require request authentication.

[Official authentication documentation](https://date.nager.at/API)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Today Public Holiday](actions/check-today-public-holiday.md) | `GET /api/v3/IsTodayPublicHoliday/{{countryCode}}` | [docs](https://date.nager.at/openapi/v3.json) |
| [Get API Version](actions/get-api-version.md) | `GET /api/v3/Version` | [docs](https://date.nager.at/openapi/v3.json) |
| [Get Country Info](actions/get-country-info.md) | `GET /api/v3/CountryInfo/{{countryCode}}` | [docs](https://date.nager.at/openapi/v3.json) |
| [List Available Countries](actions/list-available-countries.md) | `GET /api/v3/AvailableCountries` | [docs](https://date.nager.at/openapi/v3.json) |
| [List Long Weekends](actions/list-long-weekends.md) | `GET /api/v3/LongWeekend/{{year}}/{{countryCode}}` | [docs](https://date.nager.at/openapi/v3.json) |
| [List Public Holidays](actions/list-public-holidays.md) | `GET /api/v3/PublicHolidays/{{year}}/{{countryCode}}` | [docs](https://date.nager.at/API) |
| [List Upcoming Public Holidays](actions/list-upcoming-public-holidays.md) | `GET /api/v3/NextPublicHolidays/{{countryCode}}` | [docs](https://date.nager.at/openapi/v3.json) |
| [List Worldwide Upcoming Public Holidays](actions/list-worldwide-upcoming-public-holidays.md) | `GET /api/v3/NextPublicHolidaysWorldwide` | [docs](https://date.nager.at/openapi/v3.json) |
