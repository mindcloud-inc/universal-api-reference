# <img src="https://images.mindcloud.co/apps/icons/northflank_1776198674161.png" alt="Northflank logo" width="28" height="28"> Northflank: Universal API

Northflank API integration for team-scoped project, service, job, addon, secret, volume, and domain management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/northflank/latest
- **Category:** IT Operations / DevOps
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://northflank.com
- **Vendor API docs:** https://northflank.com/docs/v1/api/use-the-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/northflank/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Addon

| Action | Method | Description |
| --- | --- | --- |
| [Create addon](actions/create-addon.md) | POST | Creates a new addon in Northflank. |
| [Get addon](actions/get-addon.md) | GET | Retrieves an addon from Northflank by ID. |
| [List addons](actions/list-addons.md) | GET | Retrieves addons for a Northflank project. |

### Addon Type

| Action | Method | Description |
| --- | --- | --- |
| [List addon types](actions/list-addon-types.md) | GET | Retrieves available addon types from Northflank. |

### Api Status

| Action | Method | Description |
| --- | --- | --- |
| [Get API status](actions/get-api-status.md) | GET | Retrieves the current Northflank API status. |

### Backup Destination

| Action | Method | Description |
| --- | --- | --- |
| [List backup destinations](actions/list-backup-destinations.md) | GET | Retrieves backup destinations for your Northflank account. |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Build service](actions/build-service.md) | POST | Starts a new build for a Northflank service. |
| [Get service build](actions/get-service-build.md) | GET | Retrieves a build for a Northflank service. |

### Cloud Provider

| Action | Method | Description |
| --- | --- | --- |
| [List cloud providers](actions/list-cloud-providers.md) | GET | Retrieves available cloud providers from Northflank. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List domains](actions/list-domains.md) | GET | Retrieves available domains from your Northflank account. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create job](actions/create-job.md) | POST | Creates a new job in Northflank. |
| [Get job](actions/get-job.md) | GET | Retrieves a job from Northflank by ID. |
| [Get job run](actions/get-job-run.md) | GET | Retrieves a Northflank job run by ID. |
| [Job logs](actions/job-logs.md) | GET | Retrieves logs for a Northflank job. |
| [List jobs](actions/list-jobs.md) | GET | Retrieves jobs for a Northflank project. |
| [Trigger job run](actions/trigger-job-run.md) | POST | Starts a new job run in Northflank. |
| [Update job](actions/update-job.md) | PUT | Updates an existing job in Northflank. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List plans](actions/list-plans.md) | GET | Retrieves available plans for your Northflank account. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create project](actions/create-project.md) | POST | Creates a new project in Northflank. |
| [Delete project](actions/delete-project.md) | DELETE | Deletes an existing project from Northflank. |
| [Get project](actions/get-project.md) | GET | Retrieves a project from Northflank by ID. |
| [List projects](actions/list-projects.md) | GET | Retrieves projects for the authenticated Northflank account. |
| [Update project](actions/update-project.md) | PUT | Updates an existing project in Northflank. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List regions](actions/list-regions.md) | GET | Retrieves available regions for your Northflank account. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [List secrets](actions/list-secrets.md) | GET | Retrieves secrets for the authenticated Northflank account. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Get service](actions/get-service.md) | GET | Retrieves a service from Northflank by ID. |
| [List services](actions/list-services.md) | GET | Retrieves services for a Northflank project. |
| [Service logs](actions/service-logs.md) | GET | Retrieves logs for a Northflank service. |
| [Service metrics](actions/service-metrics.md) | GET | Retrieves metrics for a Northflank service. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List tags](actions/list-tags.md) | GET | Retrieves resource tags from your Northflank account. |

