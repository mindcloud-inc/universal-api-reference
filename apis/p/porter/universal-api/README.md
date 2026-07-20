# <img src="https://images.mindcloud.co/apps/icons/69a7462bd62d564f235e64b2-favicon_1777051862042.png" alt="Porter logo" width="28" height="28"> Porter: Universal API

Manage Porter projects, applications, clusters, and deployments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/porter/latest
- **Category:** IT Operations / DevOps
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.porter.run
- **Vendor API docs:** https://docs.porter.run/standard/cli/command-reference/porter-project

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porter/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Applications](actions/list-applications.md) | GET | Retrieves applications from a Porter project. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Logs](actions/list-audit-logs.md) | GET | Retrieves audit logs from a Porter project. |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [List Build Settings](actions/list-build-settings.md) | GET | Retrieves build settings from a Porter project. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [List Environment Groups](actions/list-environment-groups.md) | GET | Retrieves environment groups from a Porter project. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [List Project Invites](actions/list-project-invites.md) | GET | Retrieves invites from a Porter project. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Job Runs](actions/list-job-runs.md) | GET | Retrieves job runs from a Porter project. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Cloud Accounts](actions/list-cloud-accounts.md) | GET | Retrieves cloud accounts from a Porter project. |
| [List Clusters](actions/list-clusters.md) | GET | Retrieves clusters from a Porter project. |
| [List Migrations](actions/list-migrations.md) | GET | Retrieves migrations from a Porter project. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves project details from Porter. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Porter. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves services from a Porter project. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Porter. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves members from a Porter project. |

