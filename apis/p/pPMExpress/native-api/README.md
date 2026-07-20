# PPM Express: Native API Reference

A consolidated summary of PPM Express's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://help.ppm.express/public-api
- **OpenAPI specification:** https://api-us.ppm.express/v1.0/swagger.json
- **API base URL:** `https://api-us.ppm.express`

## Authentication

### Bearer Token

Use a PPM Express public API bearer token. Also provide the tenant name used in the @tenant path segment for API requests.

### Credentials

- **API Key:** `apiKey` · required
- **Tenant Name:** `tenantName` · required · The tenant slug used in the API path, without the leading @.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.ppm.express/public-api/1177822?from_search=135780420)

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Challenge](actions/get-challenge.md) | `GET /@:tenantName/v1.0/challenges/:id` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Current User](actions/get-current-user.md) | `GET /@:tenantName/v1.0/Me` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Global Work Week Hours](actions/get-global-work-week-hours.md) | `GET /@:tenantName/v1.0/calendar/workweekhours` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Idea](actions/get-idea.md) | `GET /@:tenantName/v1.0/ideas/:id` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Portfolio](actions/get-portfolio.md) | `GET /@:tenantName/v1.0/portfolios/:id` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Program](actions/get-program.md) | `GET /@:tenantName/v1.0/programs/:id` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Project](actions/get-project.md) | `GET /@:tenantName/v1.0/projects/:id` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Project Deliverable](actions/get-project-deliverable.md) | `GET /@:tenantName/v1.0/projects/:projectId/deliverables/:deliverableId` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Project Key Date](actions/get-project-key-date.md) | `GET /@:tenantName/v1.0/projects/:projectId/keydates/:keyDateId` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Project Task](actions/get-project-task.md) | `GET /@:tenantName/v1.0/projects/:projectId/tasks/:taskId` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Resource](actions/get-resource.md) | `GET /@:tenantName/v1.0/resources/:id` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Resource Work Week Hours](actions/get-resource-work-week-hours.md) | `GET /@:tenantName/v1.0/resourcecalendar/:id/workweekhours` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get Settings](actions/get-settings.md) | `GET /@:tenantName/v1.0/settings` | [docs](https://help.ppm.express/public-api/1177822) |
| [Get User](actions/get-user.md) | `GET /@:tenantName/v1.0/users/:id` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Administrative Categories](actions/list-administrative-categories.md) | `GET /@:tenantName/v1.0/timetracking/administrativecategories` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Challenge Fields](actions/list-challenge-fields.md) | `GET /@:tenantName/v1.0/fields/Challenge` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Challenges](actions/list-challenges.md) | `GET /@:tenantName/v1.0/challenges` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Global Calendar Exceptions](actions/list-global-calendar-exceptions.md) | `GET /@:tenantName/v1.0/calendar/exceptions` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Idea Fields](actions/list-idea-fields.md) | `GET /@:tenantName/v1.0/fields/Idea` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Ideas](actions/list-ideas.md) | `GET /@:tenantName/v1.0/ideas` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Key Date Fields](actions/list-key-date-fields.md) | `GET /@:tenantName/v1.0/fields/KeyDate` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Portfolio Fields](actions/list-portfolio-fields.md) | `GET /@:tenantName/v1.0/fields/Portfolio` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Portfolios](actions/list-portfolios.md) | `GET /@:tenantName/v1.0/portfolios` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Program Fields](actions/list-program-fields.md) | `GET /@:tenantName/v1.0/fields/Program` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Programs](actions/list-programs.md) | `GET /@:tenantName/v1.0/programs` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Project Deliverables](actions/list-project-deliverables.md) | `GET /@:tenantName/v1.0/projects/:projectId/deliverables` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Project Fields](actions/list-project-fields.md) | `GET /@:tenantName/v1.0/fields/Project` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Project Key Dates](actions/list-project-key-dates.md) | `GET /@:tenantName/v1.0/projects/:projectId/keydates` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Project Process Stages](actions/list-project-process-stages.md) | `GET /@:tenantName/v1.0/projects/:projectId/process/stages` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /@:tenantName/v1.0/projects/:projectId/tasks` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Projects](actions/list-projects.md) | `GET /@:tenantName/v1.0/projects` | [docs](https://help.ppm.express/time-tracking/time-tracking-and-time-tracking-suggestions-api-requests) |
| [List Resource Calendar Exceptions](actions/list-resource-calendar-exceptions.md) | `GET /@:tenantName/v1.0/resourcecalendar/:id/exceptions` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Resource Fields](actions/list-resource-fields.md) | `GET /@:tenantName/v1.0/fields/Resource` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Resources](actions/list-resources.md) | `GET /@:tenantName/v1.0/resources` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Task Fields](actions/list-task-fields.md) | `GET /@:tenantName/v1.0/fields/Task` | [docs](https://help.ppm.express/public-api/1177822) |
| [List Users](actions/list-users.md) | `GET /@:tenantName/v1.0/users` | [docs](https://help.ppm.express/public-api/1261201-working-with-webhooks-in-ppm-express) |
| [List Webhooks](actions/list-webhooks.md) | `GET /@:tenantName/v1.0/webhooks` | [docs](https://help.ppm.express/public-api/1177822) |
