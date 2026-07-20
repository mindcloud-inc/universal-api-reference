# TimeAPI: Native API Reference

A consolidated summary of TimeAPI's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.timeapi.io/swagger/index.html
- **OpenAPI specification:** https://www.timeapi.io/swagger/v1/swagger.json
- **API base URL:** `https://www.timeapi.io`

## Authentication

### No authentication

TimeAPI public endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.timeapi.io/swagger/index.html)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current Time By Coordinates](actions/get-current-time-by-coordinates.md) | `GET /api/v1/time/current/coordinate` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Current Time By IP Address](actions/get-current-time-by-ip-address.md) | `GET /api/v1/time/current/ip` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Current Time By Time Zone](actions/get-current-time-by-time-zone.md) | `GET /api/v1/time/current/zone` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Current Unix Timestamp](actions/get-current-unix-timestamp.md) | `GET /api/v1/time/current/unix` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Current Unix Timestamp Microseconds](actions/get-current-unix-timestamp-microseconds.md) | `GET /api/v1/time/current/unix_us` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Current Unix Timestamp Milliseconds](actions/get-current-unix-timestamp-milliseconds.md) | `GET /api/v1/time/current/unix_ms` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Current Unix Timestamp Nanoseconds](actions/get-current-unix-timestamp-nanoseconds.md) | `GET /api/v1/time/current/unix_ns` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Current UTC Time](actions/get-current-utc-time.md) | `GET /api/v1/time/current/utc` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Time Zone Details](actions/get-time-zone-details.md) | `GET /api/v1/timezone/zone` | [docs](https://www.timeapi.io/swagger/index.html) |
| [Get Time Zone Details By Coordinates](actions/get-time-zone-details-by-coordinates.md) | `GET /api/v1/timezone/coordinate` | [docs](https://www.timeapi.io/swagger/index.html) |
| [List Available Time Zones](actions/list-available-time-zones.md) | `GET /api/v1/timezone/availabletimezones` | [docs](https://www.timeapi.io/swagger/index.html) |
