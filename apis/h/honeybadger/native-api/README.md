# Honeybadger: Native API Reference

A consolidated summary of Honeybadger's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.honeybadger.io/api/
- **API base URL:** `https://api.honeybadger.io/v1`

## Authentication

### Reporting API key

Project API key for Honeybadger Reporting API endpoints only.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.honeybadger.io/api/getting-started/)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ping Check-in](actions/ping-check-in.md) | `GET /check_in/:checkInId` | [docs](https://docs.honeybadger.io/api/reporting-check-ins/) |
| [Ping Check-in by Slug](actions/ping-check-in-by-slug.md) | `GET /check_in/:apiKey/:checkInSlug` | [docs](https://docs.honeybadger.io/api/reporting-check-ins/) |
| [Report Check-in Details](actions/report-check-in-details.md) | `POST /check_in/:checkInId` | [docs](https://docs.honeybadger.io/api/reporting-check-ins/) |
| [Report Deployment](actions/report-deployment.md) | `POST /deploys` | [docs](https://docs.honeybadger.io/api/reporting-deployments/) |
| [Report Error](actions/report-error.md) | `POST /notices` | [docs](https://docs.honeybadger.io/api/reporting-exceptions/) |
| [Report Event](actions/report-event.md) | `POST /events` | [docs](https://docs.honeybadger.io/api/reporting-events/) |
| [Upload Source Map](actions/upload-source-map.md) | `POST /source_maps` | [docs](https://docs.honeybadger.io/api/reporting-source-maps/) |
