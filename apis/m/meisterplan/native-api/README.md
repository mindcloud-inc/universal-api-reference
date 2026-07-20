# Meisterplan: Native API Reference

A consolidated summary of Meisterplan's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.us.meisterplan.com/docs/api.html
- **OpenAPI specification:** https://api.us.meisterplan.com/swagger.json
- **API base URL:** `https://api.us.meisterplan.com/v1`

## Authentication

### API Token

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.meisterplan.com/hc/en-us/articles/360013755819-Reporting-API-Manage-API-Tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–500). Use `pageAfter` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Milestone](actions/create-milestone.md) | `POST /scenarios/:scenarioId/projects/:projectId/milestones` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/CreateMilestone) |
| [Create Or Update Allocation](actions/create-or-update-allocation.md) | `POST /scenarios/:scenarioId/projects/:projectId/allocations` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/CreateOrUpdateAllocation) |
| [Create Program](actions/create-program.md) | `POST /scenarios/:scenarioId/programs` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/CreateProgram) |
| [Create Project](actions/create-project.md) | `POST /scenarios/:scenarioId/projects` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/CreateProject) |
| [Create Resource](actions/create-resource.md) | `POST /resources` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/CreateResource) |
| [Create Role](actions/create-role.md) | `POST /roles` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/CreateRole) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/CreateTeam) |
| [Delete Allocation](actions/delete-allocation.md) | `DELETE /scenarios/:scenarioId/projects/:projectId/allocations/:allocationId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/DeleteAllocation) |
| [Delete Milestone](actions/delete-milestone.md) | `DELETE /scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/DeleteMilestone) |
| [Delete Program](actions/delete-program.md) | `DELETE /scenarios/:scenarioId/programs/:programId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/DeleteProgram) |
| [Delete Project](actions/delete-project.md) | `DELETE /scenarios/:scenarioId/projects/:projectId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/DeleteProject) |
| [Delete Resource](actions/delete-resource.md) | `DELETE /resources/:resourceId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/DeleteResource) |
| [Delete Role](actions/delete-role.md) | `DELETE /roles/:roleId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/DeleteRole) |
| [Delete Team](actions/delete-team.md) | `DELETE /teams/:teamId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/DeleteTeam) |
| [Find Or Create Resources](actions/find-or-create-resources.md) | `POST /resources/findOrCreateResources` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/FindOrCreateResources) |
| [Get Allocation](actions/get-allocation.md) | `GET /scenarios/:scenarioId/projects/:projectId/allocations/:allocationId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllocationId) |
| [Get Milestone](actions/get-milestone.md) | `GET /scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetMilestoneById) |
| [Get Program](actions/get-program.md) | `GET /scenarios/:scenarioId/programs/:programId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetProgramById) |
| [Get Project](actions/get-project.md) | `GET /scenarios/:scenarioId/projects/:projectId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetProjectById) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:resourceId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetResourceById) |
| [Get Role](actions/get-role.md) | `GET /roles/:roleId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetRoleById) |
| [Get Scenario](actions/get-scenario.md) | `GET /scenarios/:scenarioId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetScenarioById) |
| [Get Team](actions/get-team.md) | `GET /teams/:teamId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetTeamById) |
| [List Allocations](actions/list-allocations.md) | `GET /scenarios/:scenarioId/projects/:projectId/allocations` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllAllocations) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllCalendars) |
| [List Milestones](actions/list-milestones.md) | `GET /scenarios/:scenarioId/projects/:projectId/milestones` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllMilestones) |
| [List Portfolios](actions/list-portfolios.md) | `GET /portfolios` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllPortfolios) |
| [List Programs](actions/list-programs.md) | `GET /scenarios/:scenarioId/programs` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllPrograms) |
| [List Projects](actions/list-projects.md) | `GET /scenarios/:scenarioId/projects` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllProjects) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllResources) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllRoles) |
| [List Scenarios](actions/list-scenarios.md) | `GET /scenarios` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllScenarios) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/GetAllTeams) |
| [Update Allocation](actions/update-allocation.md) | `PATCH /scenarios/:scenarioId/projects/:projectId/allocations/:allocationId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/UpdateAllocation) |
| [Update Milestone](actions/update-milestone.md) | `PATCH /scenarios/:scenarioId/projects/:projectId/milestones/:milestoneId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/UpdateMilestone) |
| [Update Program](actions/update-program.md) | `PATCH /scenarios/:scenarioId/programs/:programId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/UpdateProgram) |
| [Update Project](actions/update-project.md) | `PATCH /scenarios/:scenarioId/projects/:projectId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/UpdateProject) |
| [Update Resource](actions/update-resource.md) | `PATCH /resources/:resourceId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/UpdateResource) |
| [Update Role](actions/update-role.md) | `PATCH /roles/:roleId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/UpdateRole) |
| [Update Team](actions/update-team.md) | `PATCH /teams/:teamId` | [docs](https://api.us.meisterplan.com/docs/api.html#operation/UpdateTeam) |
