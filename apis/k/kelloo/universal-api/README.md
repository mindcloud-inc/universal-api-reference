# <img src="https://images.mindcloud.co/apps/icons/kelloo_1775564834929.png" alt="Kelloo logo" width="28" height="28"> Kelloo: Universal API

Kelloo is resource planning and project portfolio management software for planning projects, resources, teams, scenarios, sprints, and work items.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kelloo/latest
- **Category:** Productivity / Project Management
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kelloo.com
- **Vendor API docs:** https://documenter.getpostman.com/view/14463756/UzBgtpF8

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Application Configuration](actions/get-application-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kelloo/latest/actions/get-application-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Application Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Configuration](actions/get-application-configuration.md) | GET | Retrieves application configuration details from Kelloo. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get All Products](actions/get-all-products.md) | GET | Retrieves all product records from Kelloo. |
| [Get All Projects](actions/get-all-projects.md) | GET | Retrieves all project records from Kelloo. |
| [Get All Resources](actions/get-all-resources.md) | GET | Retrieves all resource records from Kelloo. |
| [Get All Roles](actions/get-all-roles.md) | GET | Retrieves all role records from Kelloo. |
| [Get All Scenario Projects](actions/get-all-scenario-projects.md) | GET | Retrieves all scenario projects from Kelloo. |
| [Get All Scenarios](actions/get-all-scenarios.md) | GET | Retrieves all scenario records from Kelloo. |
| [Get All Teams](actions/get-all-teams.md) | GET | Retrieves all team records from Kelloo. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product record from Kelloo. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project record from Kelloo. |
| [Get Project Lookup Values](actions/get-project-lookup-values.md) | GET | Retrieves values for a Kelloo project lookup. |
| [Get Project Lookups](actions/get-project-lookups.md) | GET | Retrieves project lookup definitions from Kelloo. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource record from Kelloo. |
| [Get Role](actions/get-role.md) | GET | Retrieves a role record from Kelloo. |
| [Get Scenario](actions/get-scenario.md) | GET | Retrieves a scenario record from Kelloo. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team record from Kelloo. |
| [Get Work Item](actions/get-work-item.md) | GET | Retrieves a work item from Kelloo. |
| [Get Work Item Segments](actions/get-work-item-segments.md) | GET | Retrieves work item segments from Kelloo. |
| [Get Work Items](actions/get-work-items.md) | GET | Retrieves work items from Kelloo. |

