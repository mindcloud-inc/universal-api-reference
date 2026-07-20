# RoboAuditor: Native API Reference

A consolidated summary of RoboAuditor's API configuration and 19 documented operations.

- **API base URL:** `https://app.siteauditor.com/api`

## Authentication

### Login Token (Custom)

Authenticate with RoboAuditor login credentials and use Bearer access_token for API requests.

### Credentials

- **Email:** `email` · required · RoboAuditor account email.
- **Password:** `password` · required · RoboAuditor account password.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://app.siteauditor.com/js/login.6857d907.js)

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path |
| --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /login` |
| [Check URL Exists](actions/check-url-exists.md) | `GET /urlExist` |
| [Delete Domain Settings](actions/delete-domain-settings.md) | `DELETE /domain-settings/` |
| [Export Leads](actions/export-leads.md) | `GET /leads/export` |
| [Generate Report](actions/generate-report.md) | `POST /report` |
| [Get Domain Settings](actions/get-domain-settings.md) | `GET /domain-settings/` |
| [Get Lead Settings](actions/get-lead-settings.md) | `GET /lead-settings` |
| [Get Lead Token](actions/get-lead-token.md) | `POST /lead/getToken` |
| [Get Report Settings](actions/get-report-settings.md) | `GET /settings/report` |
| [Import Leads](actions/import-leads.md) | `POST /leads/import` |
| [List Blocked Leads](actions/list-blocked-leads.md) | `GET /blocked_leads` |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` |
| [List Leads](actions/list-leads.md) | `GET /leads` |
| [Reset Report Settings](actions/reset-report-settings.md) | `POST /settings/report/reset` |
| [Update Conversion Tracking](actions/update-conversion-tracking.md) | `POST /integrations/conversion-tracking` |
| [Update Domain Settings](actions/update-domain-settings.md) | `POST /domain-settings/` |
| [Update Lead Settings](actions/update-lead-settings.md) | `POST /lead-settings` |
| [Update Report Settings](actions/update-report-settings.md) | `POST /settings/report` |
| [Validate Domain Settings](actions/validate-domain-settings.md) | `GET /domain-settings/validate` |
