# Timizer: Native API Reference

A consolidated summary of Timizer's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api-doc.timizer.io
- **OpenAPI specification:** https://api-doc.timizer.io/api-key-doc.swagger.yaml
- **API base URL:** `https://api.timizer.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
timizer-api-key: <apiKey>
```

[Official authentication documentation](https://api-doc.timizer.io)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `companies`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /app/clients` | [docs](https://api-doc.timizer.io) |
| [Create Client Contact](actions/create-client-contact.md) | `POST /app/clients/:id/contacts` | [docs](https://api-doc.timizer.io) |
| [Create Contracted Company](actions/create-contracted-company.md) | `POST /app/contracted` | [docs](https://api-doc.timizer.io) |
| [Create Team Activity Report](actions/create-team-activity-report.md) | `POST /app/admin-teams/:teamId/activity-reports` | [docs](https://api-doc.timizer.io) |
| [Create Team Invitations](actions/create-team-invitations.md) | `POST /app/admin-teams/:teamId/invitations` | [docs](https://api-doc.timizer.io) |
| [Create Team Mission](actions/create-team-mission.md) | `POST /app/admin-teams/:teamId/missions` | [docs](https://api-doc.timizer.io) |
| [Delete Client](actions/delete-client.md) | `DELETE /app/clients/:id` | [docs](https://api-doc.timizer.io) |
| [Delete Client Contact](actions/delete-client-contact.md) | `DELETE /app/clients/:id/contacts/:contactId` | [docs](https://api-doc.timizer.io) |
| [Delete Contracted Company](actions/delete-contracted-company.md) | `DELETE /app/contracted/:id` | [docs](https://api-doc.timizer.io) |
| [Get Client](actions/get-client.md) | `GET /app/clients/:id` | [docs](https://api-doc.timizer.io) |
| [Get Contracted Company](actions/get-contracted-company.md) | `GET /app/contracted/:id` | [docs](https://api-doc.timizer.io) |
| [Get Team Activity Report](actions/get-team-activity-report.md) | `GET /app/admin-teams/:teamId/activity-reports/:activityReportId` | [docs](https://api-doc.timizer.io) |
| [List Client Contacts](actions/list-client-contacts.md) | `GET /app/clients/:id/contacts` | [docs](https://api-doc.timizer.io) |
| [List Clients](actions/list-clients.md) | `GET /app/clients` | [docs](https://api-doc.timizer.io) |
| [List Contracted Companies](actions/list-contracted-companies.md) | `GET /app/contracted` | [docs](https://api-doc.timizer.io) |
| [List Team Activity Reports](actions/list-team-activity-reports.md) | `GET /app/admin-teams/:teamId/activity-reports` | [docs](https://api-doc.timizer.io) |
| [List Team Members](actions/list-team-members.md) | `GET /app/admin-teams/:teamId/members` | [docs](https://api-doc.timizer.io) |
| [List Team Missions](actions/list-team-missions.md) | `GET /app/admin-teams/:teamId/missions` | [docs](https://api-doc.timizer.io) |
| [List Teams](actions/list-teams.md) | `GET /app/admin-teams` | [docs](https://api-doc.timizer.io) |
| [Share Team Activity Report](actions/share-team-activity-report.md) | `POST /app/admin-teams/:teamId/activity-reports/:activityReportId/share` | [docs](https://api-doc.timizer.io) |
| [Share Team Activity Report by Email](actions/share-team-activity-report-by-email.md) | `POST /app/admin-teams/:teamId/activity-reports/:activityReportId/share-by-email` | [docs](https://api-doc.timizer.io) |
| [Update Client](actions/update-client.md) | `PATCH /app/clients/:id` | [docs](https://api-doc.timizer.io) |
| [Update Contracted Company](actions/update-contracted-company.md) | `PATCH /app/contracted/:id` | [docs](https://api-doc.timizer.io) |
| [Update Team Activity Report](actions/update-team-activity-report.md) | `PATCH /app/admin-teams/:teamId/activity-reports/:activityReportId` | [docs](https://api-doc.timizer.io) |
