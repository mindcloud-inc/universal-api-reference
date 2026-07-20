# Timing: Native API Reference

A consolidated summary of Timing's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://web.timingapp.com/docs/
- **OpenAPI specification:** https://web.timingapp.com/docs/openapi.yaml
- **API base URL:** `https://web.timingapp.com/api/v1`

## Authentication

### API Key

Use a Timing API key generated from the Timing web app and sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://web.timingapp.com/docs/)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Update Time Entries](actions/batch-update-time-entries.md) | `PATCH /time-entries/batch-update` | [docs](https://web.timingapp.com/docs/#time-entries-PATCHapi-v1-time-entries-batch-update) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://web.timingapp.com/docs/#projects-POSTapi-v1-projects) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /time-entries` | [docs](https://web.timingapp.com/docs/#time-entries-POSTapi-v1-time-entries) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:project_id` | [docs](https://web.timingapp.com/docs/#projects-DELETEapi-v1-projects--project_id-) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /time-entries/:time_entry_id` | [docs](https://web.timingapp.com/docs/#time-entries-DELETEapi-v1-time-entries--time_entry_id-) |
| [Generate Report](actions/generate-report.md) | `GET /report` | [docs](https://web.timingapp.com/docs/#reports-GETapi-v1-report) |
| [Get Activity Hierarchy](actions/get-activity-hierarchy.md) | `GET /activity-hierarchy` | [docs](https://web.timingapp.com/docs/#activity-hierarchy-GETapi-v1-activity-hierarchy) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://web.timingapp.com/docs/#projects-GETapi-v1-projects) |
| [List Projects Hierarchically](actions/list-projects-hierarchically.md) | `GET /projects/hierarchy` | [docs](https://web.timingapp.com/docs/#projects-GETapi-v1-projects-hierarchy) |
| [List Team Members](actions/list-team-members.md) | `GET /teams/:team_id/members` | [docs](https://web.timingapp.com/docs/#teams-GETapi-v1-teams--team_id--members) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://web.timingapp.com/docs/#teams-GETapi-v1-teams) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time-entries` | [docs](https://web.timingapp.com/docs/#time-entries-GETapi-v1-time-entries) |
| [Show Latest Time Entry](actions/show-latest-time-entry.md) | `GET /time-entries/latest` | [docs](https://web.timingapp.com/docs/#time-entries-GETapi-v1-time-entries-latest) |
| [Show Project](actions/show-project.md) | `GET /projects/:project_id` | [docs](https://web.timingapp.com/docs/#projects-GETapi-v1-projects--project_id-) |
| [Show Running Timer](actions/show-running-timer.md) | `GET /time-entries/running` | [docs](https://web.timingapp.com/docs/#time-entries-GETapi-v1-time-entries-running) |
| [Show Time Entry](actions/show-time-entry.md) | `GET /time-entries/:time_entry_id` | [docs](https://web.timingapp.com/docs/#time-entries-GETapi-v1-time-entries--time_entry_id-) |
| [Start Timer](actions/start-timer.md) | `POST /time-entries/start` | [docs](https://web.timingapp.com/docs/#time-entries-POSTapi-v1-time-entries-start) |
| [Stop Timer](actions/stop-timer.md) | `PUT /time-entries/stop` | [docs](https://web.timingapp.com/docs/#time-entries-PUTapi-v1-time-entries-stop) |
| [Update Project](actions/update-project.md) | `PUT /projects/:project_id` | [docs](https://web.timingapp.com/docs/#projects-PUTapi-v1-projects--project_id-) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /time-entries/:time_entry_id` | [docs](https://web.timingapp.com/docs/#time-entries-PUTapi-v1-time-entries--time_entry_id-) |
