# PagePixels: Native API Reference

A consolidated summary of PagePixels's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://pagepixels.com/app/screenshots-api-documentation
- **API base URL:** `https://api.pagepixels.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pagepixels.com/app/screenshots-api-documentation#private-api-key)

## API conventions

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `limit` in the query string to set the page size (default 1000; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Next Scheduled Screenshot](actions/capture-next-scheduled-screenshot.md) | `POST /screenshot_configs/:screenshot_configuration_id/capture` | [docs](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-capture) |
| [Capture Screenshot](actions/capture-screenshot.md) | `GET /snap` | [docs](https://pagepixels.com/app/screenshots-api-documentation#quick-snap) |
| [Create Scheduled Screenshot](actions/create-scheduled-screenshot.md) | `POST /screenshot_configs` | [docs](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-create) |
| [Create Website Domain Research Request](actions/create-website-domain-research-request.md) | `POST /api/domain_research_requests` | [docs](https://pagepixels.com/app/screenshots-api-documentation#domain-research-create) |
| [Delete Screenshot Configuration](actions/delete-screenshot-configuration.md) | `DELETE /screenshot_configs/:screenshot_config_id` | [docs](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-delete) |
| [Get Account Limits](actions/get-account-limits.md) | `GET /account_limits` | [docs](https://pagepixels.com/app/screenshots-api-documentation#account-limits-get) |
| [Get Job Status](actions/get-job-status.md) | `GET /jobs/:job_id` | [docs](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-status) |
| [Get Screenshot Configuration](actions/get-screenshot-configuration.md) | `GET /screenshot_configs/:screenshot_configuration_id` | [docs](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-get) |
| [Get Screenshots From Configuration](actions/get-screenshots-from-configuration.md) | `GET /screenshot_configs/:screenshot_config_id/screenshots` | [docs](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-index) |
| [Get Website Domain Research Job Status](actions/get-website-domain-research-job-status.md) | `GET /api/domain_research_requests/:job_id/status` | [docs](https://pagepixels.com/app/screenshots-api-documentation#domain-research-status) |
| [Get Website Domain Research Report](actions/get-website-domain-research-report.md) | `GET /api/domain_research_requests/:job_id/report` | [docs](https://pagepixels.com/app/screenshots-api-documentation#domain-research-report) |
| [List All Change Notifications](actions/list-all-change-notifications.md) | `GET /change_notifications` | [docs](https://pagepixels.com/app/screenshots-api-documentation#show-all-changes-all) |
| [List All Screenshots](actions/list-all-screenshots.md) | `GET /screenshots` | [docs](https://pagepixels.com/app/screenshots-api-documentation#list-all-screenshots) |
| [List All Website Domain Research Reports](actions/list-all-website-domain-research-reports.md) | `GET /api/domain_research_requests` | [docs](https://pagepixels.com/app/screenshots-api-documentation#list-all-domain-research-reports) |
| [List Change Notifications](actions/list-change-notifications.md) | `GET /screenshot_configs/:screenshot_config_id/change_notifications` | [docs](https://pagepixels.com/app/screenshots-api-documentation#show-all-changes) |
| [List Real Locations](actions/list-real-locations.md) | `GET /real_locations` | [docs](https://pagepixels.com/app/screenshots-api-documentation#real-locations-get) |
| [List Screenshot Configurations](actions/list-screenshot-configurations.md) | `GET /screenshot_configs` | [docs](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-list-all) |
