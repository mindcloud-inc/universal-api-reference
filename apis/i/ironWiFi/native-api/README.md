# IronWiFi: Native API Reference

A consolidated summary of IronWiFi's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://api.ironwifi.com/
- **OpenAPI specification:** https://api.ironwifi.com/
- **API base URL:** `https://console.ironwifi.com/api`

## Authentication

### API Key (Implicit)

Authenticate to IronWiFi with an API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.ironwifi.com/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json;charset=utf-8` |

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Accounting Report](actions/get-accounting-report.md) | `GET /reports/111` | [docs](https://api.ironwifi.com/) |
| [Get Authentication Report](actions/get-authentication-report.md) | `GET /reports/110` | [docs](https://api.ironwifi.com/) |
| [List Access Points](actions/list-access-points.md) | `GET /nodes` | [docs](https://api.ironwifi.com/) |
| [List Attributes](actions/list-attributes.md) | `GET /attributes` | [docs](https://api.ironwifi.com/) |
| [List Captive Portals](actions/list-captive-portals.md) | `GET /captive-portals` | [docs](https://api.ironwifi.com/) |
| [List Configurations](actions/list-configurations.md) | `GET /configurations` | [docs](https://api.ironwifi.com/) |
| [List Connectors](actions/list-connectors.md) | `GET /connectors` | [docs](https://api.ironwifi.com/) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://api.ironwifi.com/) |
| [List Employees](actions/list-employees.md) | `GET /employees` | [docs](https://api.ironwifi.com/) |
| [List Fleets](actions/list-fleets.md) | `GET /fleets` | [docs](https://api.ironwifi.com/) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://api.ironwifi.com/) |
| [List Guest Profiles](actions/list-guest-profiles.md) | `GET /guest-profiles` | [docs](https://api.ironwifi.com/) |
| [List Guests](actions/list-guests.md) | `GET /guests` | [docs](https://api.ironwifi.com/) |
| [List Networks](actions/list-networks.md) | `GET /networks` | [docs](https://api.ironwifi.com/) |
| [List Org Unit Group Mappings](actions/list-org-unit-group-mappings.md) | `GET /org-units-groups` | [docs](https://api.ironwifi.com/) |
| [List Organization Units](actions/list-organization-units.md) | `GET /orgunits` | [docs](https://api.ironwifi.com/) |
| [List Shared Files](actions/list-shared-files.md) | `GET /shared-files` | [docs](https://api.ironwifi.com/) |
| [List Tariff Groups](actions/list-tariff-groups.md) | `GET /tariff-groups` | [docs](https://api.ironwifi.com/) |
| [List Tariffs](actions/list-tariffs.md) | `GET /tariffs` | [docs](https://api.ironwifi.com/) |
| [List Themes](actions/list-themes.md) | `GET /themes` | [docs](https://api.ironwifi.com/) |
| [List Translations](actions/list-translations.md) | `GET /translations` | [docs](https://api.ironwifi.com/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.ironwifi.com/) |
| [List Variables](actions/list-variables.md) | `GET /variables` | [docs](https://api.ironwifi.com/) |
| [List Vehicles](actions/list-vehicles.md) | `GET /vehicles` | [docs](https://api.ironwifi.com/) |
| [List Venues](actions/list-venues.md) | `GET /venues` | [docs](https://api.ironwifi.com/) |
| [List Vouchers](actions/list-vouchers.md) | `GET /vouchers` | [docs](https://api.ironwifi.com/) |
