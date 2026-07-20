# <img src="https://images.mindcloud.co/apps/icons/dremio-icon_1775836514498.png" alt="Dremio logo" width="28" height="28"> Dremio: Universal API

Dremio Cloud API for projects, catalog objects, SQL jobs, scripts, reflections, search, and source administration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dremio/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 63
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dremio.com/
- **Vendor API docs:** https://docs.dremio.com/dremio-cloud/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Catalog](actions/list-catalog.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-catalog?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (63)

### Catalog Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Catalog](actions/list-catalog.md) | GET | Retrieves catalog entries from a Dremio project. |

### Catalog Grants

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Grants](actions/get-catalog-grants.md) | GET | Retrieves grants for a catalog entry in Dremio. |
| [Update Catalog Grants](actions/update-catalog-grants.md) | PUT | Updates grants for a catalog entry in Dremio. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET |  |

### Engine

| Action | Method | Description |
| --- | --- | --- |
| [Create Engine](actions/create-engine.md) | POST | Creates a new engine in a Dremio project. |
| [Delete Engine](actions/delete-engine.md) | DELETE | Deletes an existing engine from a Dremio project. |
| [Disable Engine](actions/disable-engine.md) | PUT | Disables an engine in a Dremio project. |
| [Enable Engine](actions/enable-engine.md) | PUT | Enables an engine in a Dremio project. |
| [Get Engine](actions/get-engine.md) | GET | Retrieves an engine from a Dremio project. |
| [List Engines](actions/list-engines.md) | GET | Retrieves engines from a Dremio project. |
| [Update Engine](actions/update-engine.md) | PUT | Updates an existing engine in a Dremio project. |

### Engine Rules

| Action | Method | Description |
| --- | --- | --- |
| [List Engine Rules](actions/list-engine-rules.md) | GET | Retrieves engine rules from a Dremio project. |

### External Token Provider

| Action | Method | Description |
| --- | --- | --- |
| [Create External Token Provider](actions/create-external-token-provider.md) | POST | Creates a new external token provider in Dremio. |
| [Delete External Token Provider](actions/delete-external-token-provider.md) | DELETE | Deletes an external token provider from Dremio. |
| [Disable External Token Provider](actions/disable-external-token-provider.md) | PUT | Disables an external token provider in Dremio. |
| [Enable External Token Provider](actions/enable-external-token-provider.md) | PUT | Enables an external token provider in Dremio. |
| [Get External Token Provider](actions/get-external-token-provider.md) | GET | Retrieves an external token provider from Dremio by ID. |
| [List External Token Providers](actions/list-external-token-providers.md) | GET | Retrieves external token providers from Dremio. |
| [Update External Token Provider](actions/update-external-token-provider.md) | PUT | Updates an external token provider in Dremio. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from a Dremio project. |

### Identity Provider

| Action | Method | Description |
| --- | --- | --- |
| [Create Identity Provider](actions/create-identity-provider.md) | POST | Creates a new identity provider in Dremio. |
| [Delete Identity Provider](actions/delete-identity-provider.md) | DELETE | Deletes an identity provider from Dremio. |
| [Disable Identity Provider](actions/disable-identity-provider.md) | PUT | Disables an identity provider in Dremio. |
| [Enable Identity Provider](actions/enable-identity-provider.md) | PUT | Enables an identity provider in Dremio. |
| [Get Identity Provider](actions/get-identity-provider.md) | GET | Retrieves an identity provider from Dremio by ID. |
| [List Identity Providers](actions/list-identity-providers.md) | GET | Retrieves identity providers from Dremio. |
| [Update Identity Provider](actions/update-identity-provider.md) | PUT | Updates an identity provider in Dremio. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | PUT | Cancels a job in a Dremio project. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from a Dremio project. |

### Job Results

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Results](actions/get-job-results.md) | GET | Retrieves results for a Dremio job. |

### Maintenance Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Maintenance Task](actions/create-maintenance-task.md) | POST | Creates a new maintenance task in a Dremio project. |
| [Delete Maintenance Task](actions/delete-maintenance-task.md) | DELETE | Deletes an existing maintenance task from a Dremio project. |
| [Get Maintenance Task](actions/get-maintenance-task.md) | GET | Retrieves a maintenance task from a Dremio project. |
| [List Maintenance Tasks](actions/list-maintenance-tasks.md) | GET | Retrieves maintenance tasks from a Dremio project. |
| [Update Maintenance Task](actions/update-maintenance-task.md) | PUT | Updates an existing maintenance task in a Dremio project. |

### Personal Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Personal Access Token](actions/create-personal-access-token.md) | POST | Creates a new personal access token in Dremio. |
| [Delete Personal Access Token](actions/delete-personal-access-token.md) | DELETE | Deletes personal access tokens for a Dremio user. |
| [Delete Personal Access Token By ID](actions/delete-personal-access-token-by-id.md) | DELETE | Deletes a personal access token from Dremio by ID. |
| [Get Personal Access Tokens](actions/get-personal-access-tokens.md) | GET | Retrieves personal access tokens for a Dremio user. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Dremio. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Dremio. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Dremio by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Dremio. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Dremio. |

### Reflection

| Action | Method | Description |
| --- | --- | --- |
| [Create Reflection](actions/create-reflection.md) | POST | Creates a new reflection in a Dremio project. |
| [Delete Reflection](actions/delete-reflection.md) | DELETE | Deletes an existing reflection from a Dremio project. |
| [Get Reflection Summary](actions/get-reflection-summary.md) | GET | Retrieves a reflection summary from Dremio. |
| [List Dataset Reflections](actions/list-dataset-reflections.md) | GET | Retrieves reflections for a dataset in Dremio. |
| [List Reflections](actions/list-reflections.md) | GET | Retrieves reflections from a Dremio project. |
| [Update Reflection](actions/update-reflection.md) | PUT | Updates an existing reflection in a Dremio project. |

### Reflection Refresh

| Action | Method | Description |
| --- | --- | --- |
| [Refresh Reflection](actions/refresh-reflection.md) | PUT | Refreshes an existing reflection in a Dremio project. |

### Script

| Action | Method | Description |
| --- | --- | --- |
| [Create Script](actions/create-script.md) | POST | Creates a new script in a Dremio project. |
| [Delete Script](actions/delete-script.md) | DELETE | Deletes an existing script from a Dremio project. |
| [Get Script](actions/get-script.md) | GET | Retrieves a script from a Dremio project. |
| [List Scripts](actions/list-scripts.md) | GET | Retrieves scripts from a Dremio project. |
| [Update Script](actions/update-script.md) | PUT | Updates an existing script in a Dremio project. |

### Script Batch Delete

| Action | Method | Description |
| --- | --- | --- |
| [Batch Delete Scripts](actions/batch-delete-scripts.md) | DELETE | Deletes scripts from a Dremio project in batch. |

### Script Grants

| Action | Method | Description |
| --- | --- | --- |
| [Get Script Grants](actions/get-script-grants.md) | GET | Retrieves grants for a script in Dremio. |
| [Update Script Grants](actions/update-script-grants.md) | PUT | Updates grants for a script in Dremio. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Searches a Dremio project for matching resources. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Source](actions/get-source.md) | GET | Retrieves a source from a Dremio project. |

### Source Permission Cache

| Action | Method | Description |
| --- | --- | --- |
| [Clear Source Permission Cache](actions/clear-source-permission-cache.md) | DELETE | Clears a source permission cache in Dremio. |

### Sql Job

| Action | Method | Description |
| --- | --- | --- |
| [Submit SQL Query](actions/submit-sql-query.md) | POST | Creates a SQL job in a Dremio project. |

