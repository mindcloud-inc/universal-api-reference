# <img src="https://images.mindcloud.co/apps/icons/favicon-y4jpfl_1776269899954.png" alt="Hasura logo" width="28" height="28"> Hasura: Universal API

Manage Hasura Cloud projects and tenant metadata through the Hasura Cloud GraphQL API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hasura/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hasura.io
- **Vendor API docs:** https://hasura.io/docs/2.0/api-reference/cloud-api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Hasura Cloud. |
| [Delete Tenant](actions/delete-tenant.md) | DELETE | Deletes a tenant from Hasura Cloud. |
| [Get Project Tenant ID](actions/get-project-tenant-id.md) | GET | Retrieves a Hasura project tenant ID. |
| [Get Tenant Details](actions/get-tenant-details.md) | GET | Retrieves tenant details from Hasura Cloud. |
| [Get Tenant ENV Vars](actions/get-tenant-env-vars.md) | GET | Retrieves tenant environment variables from Hasura Cloud. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Hasura Cloud. |
| [Update Tenant ENV Vars](actions/update-tenant-env-vars.md) | PUT | Updates tenant environment variables in Hasura Cloud. |

