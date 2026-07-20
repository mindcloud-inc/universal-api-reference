# <img src="https://images.mindcloud.co/apps/icons/meisterplan_1774469654432.png" alt="Meisterplan logo" width="28" height="28"> Meisterplan: Universal API

Coordinate people across teams and initiatives

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/meisterplan/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://meisterplan.com
- **Vendor API docs:** https://api.us.meisterplan.com/docs/api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Scenarios](actions/list-scenarios.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/list-scenarios?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves a list of calendars from Meisterplan. |

### Milestones

| Action | Method | Description |
| --- | --- | --- |
| [Create Milestone](actions/create-milestone.md) | POST | Creates a new milestone in Meisterplan. |
| [Get Milestone](actions/get-milestone.md) | GET | Retrieves a milestone from Meisterplan. |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves a list of milestones from Meisterplan. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Allocation](actions/create-or-update-allocation.md) | POST | Creates or updates project allocations in Meisterplan. |
| [Delete Allocation](actions/delete-allocation.md) | DELETE | Deletes an existing project allocation from Meisterplan. |
| [Delete Milestone](actions/delete-milestone.md) | DELETE | Deletes an existing milestone from Meisterplan. |
| [Get Allocation](actions/get-allocation.md) | GET | Retrieves a project allocation from Meisterplan. |
| [List Allocations](actions/list-allocations.md) | GET | Retrieves a list of project allocations from Meisterplan. |
| [Update Allocation](actions/update-allocation.md) | PUT | Updates an existing project allocation in Meisterplan. |
| [Update Milestone](actions/update-milestone.md) | PUT | Updates an existing milestone in Meisterplan. |

### Portfolio

| Action | Method | Description |
| --- | --- | --- |
| [List Portfolios](actions/list-portfolios.md) | GET | Retrieves a list of portfolios from Meisterplan. |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [Create Program](actions/create-program.md) | POST | Creates a new program in Meisterplan. |
| [Delete Program](actions/delete-program.md) | DELETE | Deletes an existing program from Meisterplan. |
| [Get Program](actions/get-program.md) | GET | Retrieves a program from Meisterplan. |
| [List Programs](actions/list-programs.md) | GET | Retrieves a list of programs from Meisterplan. |
| [Update Program](actions/update-program.md) | PUT | Updates an existing program in Meisterplan. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Meisterplan. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Meisterplan. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Meisterplan. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Meisterplan. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Meisterplan. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in Meisterplan. |
| [Delete Resource](actions/delete-resource.md) | DELETE | Deletes an existing resource from Meisterplan. |
| [Find Or Create Resources](actions/find-or-create-resources.md) | POST | Finds resources in Meisterplan, or creates them if needed. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from Meisterplan. |
| [List Resources](actions/list-resources.md) | GET | Retrieves a list of resources from Meisterplan. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Meisterplan. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a new role in Meisterplan. |
| [Delete Role](actions/delete-role.md) | DELETE | Deletes an existing role from Meisterplan. |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from Meisterplan. |
| [List Roles](actions/list-roles.md) | GET | Retrieves a list of roles from Meisterplan. |
| [Update Role](actions/update-role.md) | PUT | Updates an existing role in Meisterplan. |

### Scenario

| Action | Method | Description |
| --- | --- | --- |
| [Get Scenario](actions/get-scenario.md) | GET | Retrieves a scenario from Meisterplan. |
| [List Scenarios](actions/list-scenarios.md) | GET | Retrieves a list of scenarios from Meisterplan. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in Meisterplan. |
| [Delete Team](actions/delete-team.md) | DELETE | Deletes an existing team from Meisterplan. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Meisterplan. |
| [List Teams](actions/list-teams.md) | GET | Retrieves a list of teams from Meisterplan. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in Meisterplan. |

