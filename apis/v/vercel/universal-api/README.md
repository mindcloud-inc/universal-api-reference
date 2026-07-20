# <img src="https://images.mindcloud.co/apps/icons/vercel_1775838299601.png" alt="Vercel logo" width="28" height="28"> Vercel: Universal API

Deploy web projects and manage domains, teams, and edge configs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vercel/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vercel.com
- **Vendor API docs:** https://vercel.com/docs/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Alias

| Action | Method | Description |
| --- | --- | --- |
| [Assign Alias](actions/assign-alias.md) | POST | Assigns an alias to a Vercel deployment. |
| [Delete Alias](actions/delete-alias.md) | DELETE | Deletes an existing alias from Vercel. |
| [Get Alias](actions/get-alias.md) | GET | Retrieves an alias record from Vercel. |
| [List Aliases](actions/list-aliases.md) | GET | Retrieves all alias records from Vercel. |

### Deployment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Deployment](actions/cancel-deployment.md) | PUT | Cancels an existing deployment in Vercel. |
| [Create Deployment](actions/create-deployment.md) | POST | Creates a new deployment in Vercel. |
| [Delete Deployment](actions/delete-deployment.md) | DELETE | Deletes an existing deployment from Vercel. |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves a deployment record from Vercel. |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves all deployment records from Vercel. |

### Deployment Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment Events](actions/get-deployment-events.md) | GET | Retrieves deployment events for a Vercel deployment. |

### Deployment File

| Action | Method | Description |
| --- | --- | --- |
| [List Deployment Files](actions/list-deployment-files.md) | GET | Retrieves all deployment files from Vercel. |

### Dns Record

| Action | Method | Description |
| --- | --- | --- |
| [Create DNS Record](actions/create-dns-record.md) | POST | Creates a DNS record in Vercel. |
| [Delete DNS Record](actions/delete-dns-record.md) | DELETE | Deletes an existing DNS record from Vercel. |
| [List DNS Records](actions/list-dns-records.md) | GET | Retrieves all DNS records from Vercel. |
| [Update DNS Record](actions/update-dns-record.md) | PUT | Updates an existing DNS record in Vercel. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | POST | Adds an existing domain to Vercel. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing domain from Vercel. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain record from Vercel. |
| [List Domains](actions/list-domains.md) | GET | Retrieves all domain records from Vercel. |

### Domain Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Config](actions/get-domain-config.md) | GET | Retrieves a domain configuration from Vercel. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Vercel. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Vercel. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project record from Vercel. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from Vercel. |
| [Pause Project](actions/pause-project.md) | PUT | Pauses an existing project in Vercel. |
| [Unpause Project](actions/unpause-project.md) | PUT | Unpauses an existing project in Vercel. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Vercel. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Domain](actions/add-project-domain.md) | POST | Adds a domain to a Vercel project. |
| [Create Project Env Vars](actions/create-project-env-vars.md) | POST | Creates project environment variables in Vercel. |
| [Delete Project Env Var](actions/delete-project-env-var.md) | DELETE | Deletes an existing project environment variable from Vercel. |
| [Get Project Domain](actions/get-project-domain.md) | GET | Retrieves a project domain from Vercel. |
| [Get Project Env Var](actions/get-project-env-var.md) | GET | Retrieves a project environment variable from Vercel. |
| [List Project Domains](actions/list-project-domains.md) | GET | Retrieves all project domains from Vercel. |
| [List Project Env Vars](actions/list-project-env-vars.md) | GET | Retrieves project environment variables from Vercel. |
| [Remove Project Domain](actions/remove-project-domain.md) | DELETE | Removes a domain from a Vercel project. |
| [Update Project Domain](actions/update-project-domain.md) | PUT | Updates an existing project domain in Vercel. |
| [Update Project Env Var](actions/update-project-env-var.md) | PUT | Updates an existing project environment variable in Vercel. |
| [Verify Project Domain](actions/verify-project-domain.md) | PUT | Verifies a project domain in Vercel. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves all team records from Vercel. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the authenticated user from Vercel. |

