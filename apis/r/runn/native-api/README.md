# Runn: Native API Reference

A consolidated summary of Runn's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://developer.runn.io/reference
- **OpenAPI specification:** https://developer.runn.io/openapi/v1.0.0.json
- **API base URL:** `https://api.runn.io`

## Authentication

### Bearer Token

Authenticate with a Runn API token sent as Bearer in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required · Paste your Runn API token from Settings > API. MindCloud sends it as a Bearer token.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.runn.io/docs/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept-Version` | `1.0.0` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | `GET /clients/{{clientId}}` | [docs](https://developer.runn.io/reference/get_clients-clientid) |
| [Get Current User](actions/get-current-user.md) | `GET /me/` | [docs](https://developer.runn.io/reference/get_me) |
| [Get Holiday Group](actions/get-holiday-group.md) | `GET /holiday-groups/{{holidayGroupId}}` | [docs](https://developer.runn.io/reference/get_holiday-groups-holidaygroupid) |
| [Get Person](actions/get-person.md) | `GET /people/{{personId}}` | [docs](https://developer.runn.io/reference/get_people-personid) |
| [Get Person Current Team](actions/get-person-current-team.md) | `GET /people/{{personId}}/teams/current` | [docs](https://developer.runn.io/reference/get_people-personid-teams-current) |
| [Get Project](actions/get-project.md) | `GET /projects/{{projectId}}` | [docs](https://developer.runn.io/reference/get_projects-projectid) |
| [Get Project Total](actions/get-project-total.md) | `GET /reports/totals/projects/{{projectId}}` | [docs](https://developer.runn.io/reference/get_reports-totals-projects-projectid) |
| [Get Rate Card](actions/get-rate-card.md) | `GET /rate-cards/{{rateCardId}}` | [docs](https://developer.runn.io/reference/get_rate-cards-ratecardid) |
| [Get Role](actions/get-role.md) | `GET /roles/{{roleId}}` | [docs](https://developer.runn.io/reference/get_roles-roleid) |
| [Get Skill](actions/get-skill.md) | `GET /skills/{{skillId}}` | [docs](https://developer.runn.io/reference/get_skills-skillid) |
| [Get Team](actions/get-team.md) | `GET /teams/{{teamId}}/` | [docs](https://developer.runn.io/reference/get_teams-teamid) |
| [Get User](actions/get-user.md) | `GET /users/{{userId}}` | [docs](https://developer.runn.io/reference/get_users-userid) |
| [List Assignments](actions/list-assignments.md) | `GET /assignments/` | [docs](https://developer.runn.io/reference/get_assignments) |
| [List Client Projects](actions/list-client-projects.md) | `GET /clients/{{clientId}}/projects/` | [docs](https://developer.runn.io/reference/get_clients-clientid-projects) |
| [List Clients](actions/list-clients.md) | `GET /clients/` | [docs](https://developer.runn.io/reference/get_clients) |
| [List Holiday Group Holidays](actions/list-holiday-group-holidays.md) | `GET /holiday-groups/{{holidayGroupId}}/holidays` | [docs](https://developer.runn.io/reference/get_holiday-groups-holidaygroupid-holidays) |
| [List Holiday Groups](actions/list-holiday-groups.md) | `GET /holiday-groups/` | [docs](https://developer.runn.io/reference/get_holiday-groups) |
| [List Milestones](actions/list-milestones.md) | `GET /milestones/` | [docs](https://developer.runn.io/reference/get_milestones) |
| [List People](actions/list-people.md) | `GET /people/` | [docs](https://developer.runn.io/reference/get_people) |
| [List Person Assignments](actions/list-person-assignments.md) | `GET /people/{{personId}}/assignments/` | [docs](https://developer.runn.io/reference/get_people-personid-assignments) |
| [List Person Holiday Time Off](actions/list-person-holiday-time-off.md) | `GET /people/{{personId}}/time-offs/holidays` | [docs](https://developer.runn.io/reference/get_people-personid-time-offs-holidays) |
| [List Person Hour Report](actions/list-person-hour-report.md) | `GET /reports/hours/people/{{personId}}` | [docs](https://developer.runn.io/reference/get_reports-hours-people-personid) |
| [List Person Leave Time Off](actions/list-person-leave-time-off.md) | `GET /people/{{personId}}/time-offs/leave` | [docs](https://developer.runn.io/reference/get_people-personid-time-offs-leave) |
| [List Person Projects](actions/list-person-projects.md) | `GET /people/{{personId}}/projects/` | [docs](https://developer.runn.io/reference/get_people-personid-projects) |
| [List Person Rostered Off Time Off](actions/list-person-rostered-off-time-off.md) | `GET /people/{{personId}}/time-offs/rostered-off` | [docs](https://developer.runn.io/reference/get_people-personid-time-offs-rostered-off) |
| [List Person Skills](actions/list-person-skills.md) | `GET /people/{{personId}}/skills/` | [docs](https://developer.runn.io/reference/get_people-personid-skills) |
| [List Project Assignments](actions/list-project-assignments.md) | `GET /projects/{{projectId}}/assignments/` | [docs](https://developer.runn.io/reference/get_projects-projectid-assignments) |
| [List Project Hour Report](actions/list-project-hour-report.md) | `GET /reports/hours/projects/{{projectId}}` | [docs](https://developer.runn.io/reference/get_reports-hours-projects-projectid) |
| [List Project Milestones](actions/list-project-milestones.md) | `GET /projects/{{projectId}}/milestones/` | [docs](https://developer.runn.io/reference/get_projects-projectid-milestones) |
| [List Project People](actions/list-project-people.md) | `GET /projects/{{projectId}}/people/` | [docs](https://developer.runn.io/reference/get_projects-projectid-people) |
| [List Project Phases](actions/list-project-phases.md) | `GET /projects/{{projectId}}/phases/` | [docs](https://developer.runn.io/reference/get_projects-projectid-phases) |
| [List Project Rates](actions/list-project-rates.md) | `GET /projects/{{projectId}}/project-rates/` | [docs](https://developer.runn.io/reference/get_projects-projectid-project-rates) |
| [List Project Totals](actions/list-project-totals.md) | `GET /reports/totals/projects/` | [docs](https://developer.runn.io/reference/get_reports-totals-projects) |
| [List Project Workstreams](actions/list-project-workstreams.md) | `GET /projects/{{projectId}}/project-workstreams/` | [docs](https://developer.runn.io/reference/get_projects-projectid-project-workstreams) |
| [List Projects](actions/list-projects.md) | `GET /projects/` | [docs](https://developer.runn.io/reference/get_projects) |
| [List Rate Cards](actions/list-rate-cards.md) | `GET /rate-cards/` | [docs](https://developer.runn.io/reference/get_rate-cards) |
| [List Roles](actions/list-roles.md) | `GET /roles/` | [docs](https://developer.runn.io/reference/get_roles) |
| [List Skill People](actions/list-skill-people.md) | `GET /skills/{{skillId}}/people/` | [docs](https://developer.runn.io/reference/get_skills-skillid-people) |
| [List Skills](actions/list-skills.md) | `GET /skills/` | [docs](https://developer.runn.io/reference/get_skills) |
| [List Team People](actions/list-team-people.md) | `GET /teams/{{teamId}}/people/` | [docs](https://developer.runn.io/reference/get_teams-teamid-people) |
| [List Teams](actions/list-teams.md) | `GET /teams/` | [docs](https://developer.runn.io/reference/get_teams) |
| [List Users](actions/list-users.md) | `GET /users/` | [docs](https://developer.runn.io/reference/get_users) |
