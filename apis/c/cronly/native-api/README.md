# Cronly: Native API Reference

A consolidated summary of Cronly's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.cronly.app/
- **API base URL:** `https://cronly.app`

## Authentication

### API Token

Use a Cronly API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cronly.app/api/how-to-use-the-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Backup](actions/create-backup.md) | `POST /api/backups` | [docs](https://docs.cronly.app/api/back-ups) |
| [Create Job Monitor](actions/create-job-monitor.md) | `POST /api/monitors` | [docs](https://docs.cronly.app/api/cron-job-monitor-2) |
| [Create Project](actions/create-project.md) | `POST /api/projects` | [docs](https://docs.cronly.app/api/cron-job-monitor-3) |
| [Create Server](actions/create-server.md) | `POST /api/servers` | [docs](https://docs.cronly.app/api/servers) |
| [Create SSL Certificate Monitor](actions/create-ssl-certificate-monitor.md) | `POST /api/certificates` | [docs](https://docs.cronly.app/api/cron-job-monitor-4) |
| [Delete Backup](actions/delete-backup.md) | `DELETE /api/backups/:server_id/:username` | [docs](https://docs.cronly.app/api/back-ups) |
| [Delete Job Monitor](actions/delete-job-monitor.md) | `DELETE /api/monitors/:id` | [docs](https://docs.cronly.app/api/cron-job-monitor-2) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/projects/:id` | [docs](https://docs.cronly.app/api/cron-job-monitor-3) |
| [Delete SSL Certificate Monitor](actions/delete-ssl-certificate-monitor.md) | `DELETE /api/certificates/:id` | [docs](https://docs.cronly.app/api/cron-job-monitor-4) |
| [Get Backup](actions/get-backup.md) | `GET /api/backups/:server_id/:username` | [docs](https://docs.cronly.app/api/back-ups) |
| [Get Company](actions/get-company.md) | `GET /api/companies` | [docs](https://docs.cronly.app/api/cron-job-monitor) |
| [Get Job Monitor](actions/get-job-monitor.md) | `GET /api/monitors/:id` | [docs](https://docs.cronly.app/api/cron-job-monitor-2) |
| [Get Project](actions/get-project.md) | `GET /api/projects/:id` | [docs](https://docs.cronly.app/api/cron-job-monitor-3) |
| [Get Server](actions/get-server.md) | `GET /api/servers/:id` | [docs](https://docs.cronly.app/api/servers) |
| [Get SSL Certificate Monitor](actions/get-ssl-certificate-monitor.md) | `GET /api/certificates/:id` | [docs](https://docs.cronly.app/api/cron-job-monitor-4) |
| [Get User](actions/get-user.md) | `GET /api/users/:id` | [docs](https://docs.cronly.app/api/cron-job-monitor-5) |
| [List Backups](actions/list-backups.md) | `GET /api/backups` | [docs](https://docs.cronly.app/api/back-ups) |
| [List Job Monitors](actions/list-job-monitors.md) | `GET /api/monitors` | [docs](https://docs.cronly.app/api/cron-job-monitor-2) |
| [List Notifications](actions/list-notifications.md) | `GET /api/notifications` | [docs](https://docs.cronly.app/api/cron-job-monitor-1) |
| [List Projects](actions/list-projects.md) | `GET /api/projects` | [docs](https://docs.cronly.app/api/cron-job-monitor-3) |
| [List Servers](actions/list-servers.md) | `GET /api/servers` | [docs](https://docs.cronly.app/api/servers) |
| [List SSL Certificate Monitors](actions/list-ssl-certificate-monitors.md) | `GET /api/certificates` | [docs](https://docs.cronly.app/api/cron-job-monitor-4) |
| [List Users](actions/list-users.md) | `GET /api/users` | [docs](https://docs.cronly.app/api/cron-job-monitor-5) |
| [Send Monitor Pulse](actions/send-monitor-pulse.md) | `GET /api/monitors/pulse/:token` | [docs](https://docs.cronly.app/api/how-to-use-the-api) |
