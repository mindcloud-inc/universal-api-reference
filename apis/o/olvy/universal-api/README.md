# <img src="https://images.mindcloud.co/apps/icons/olvy_1775164879518.png" alt="Olvy logo" width="28" height="28"> Olvy: Universal API

Olvy centralizes customer feedback, issues, contacts, release notes, and surveys in a workspace-scoped GraphQL API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/olvy/latest
- **Category:** Support / Customer Success
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://olvy.co
- **Vendor API docs:** https://app.olvy.co/settings/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query](actions/query.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olvy/latest/actions/query?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves category details from Olvy. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Olvy. |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address in Olvy. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from Olvy. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Olvy. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Organisation](actions/get-organisation.md) | GET | Retrieves organisation details from Olvy. |
| [Query](actions/query.md) | GET | Makes an authenticated raw API request to Olvy. |

