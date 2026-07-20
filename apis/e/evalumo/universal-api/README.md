# <img src="https://images.mindcloud.co/apps/icons/evalumo_1774977928938.png" alt="Evalumo logo" width="28" height="28"> Evalumo: Universal API

Create projects, estimate costs, and manage construction workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/evalumo/latest
- **Category:** Productivity / Project Management
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.evalumo.com
- **Vendor API docs:** https://evalumo.apidocumentation.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalumo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Exported Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Exported Project](actions/get-exported-project.md) | GET | Finds an exported project in Evalumo by ID or name. |
| [List Exported Projects](actions/list-exported-projects.md) | GET | Retrieves exported project records from your Evalumo account. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Update Project Category](actions/update-project-category.md) | PUT | Updates a project category in Evalumo. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Evalumo. |
| [List Projects](actions/list-projects.md) | GET | Retrieves project records from your Evalumo account. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Evalumo. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Evalumo. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe To Export Webhook](actions/subscribe-to-export-webhook.md) | POST | Creates an export webhook subscription in Evalumo. |

