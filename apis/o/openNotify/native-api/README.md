# Open Notify: Native API Reference

A consolidated summary of Open Notify's API configuration and 2 documented operations.

- **API base URL:** `http://api.open-notify.org`

## Authentication

### No authentication

Open Notify public endpoints do not require authentication.

This API does not require request authentication.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current ISS Position](actions/get-current-iss-position.md) | `GET /iss-now.json` | [docs](https://open-notify.org/Open-Notify-API/ISS-Location-Now/) |
| [Get People Currently in Space](actions/get-people-currently-in-space.md) | `GET /astros.json` | [docs](https://open-notify.org/Open-Notify-API/People-In-Space/) |
