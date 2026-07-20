# Northflank: Native API Reference

A consolidated summary of Northflank's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://northflank.com/docs/v1/api/use-the-api
- **OpenAPI specification:** https://api.northflank.com/v1/swagger-json
- **API base URL:** `https://api.northflank.com/v1`

## Authentication

### Team API token

Northflank team-scoped API token authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://northflank.com/docs/v1/application/secure/manage-api-tokens)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Build service](actions/build-service.md) | `POST /projects/{projectId}/services/{serviceId}/build` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Create addon](actions/create-addon.md) | `POST /projects/{projectId}/addons` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Create job](actions/create-job.md) | `POST /projects/{projectId}/jobs` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Create project](actions/create-project.md) | `POST /projects` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Delete project](actions/delete-project.md) | `DELETE /projects/{projectId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Get addon](actions/get-addon.md) | `GET /projects/{projectId}/addons/{addonId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Get API status](actions/get-api-status.md) | `GET /` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Get job](actions/get-job.md) | `GET /projects/{projectId}/jobs/{jobId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Get job run](actions/get-job-run.md) | `GET /projects/{projectId}/jobs/{jobId}/runs/{runId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Get project](actions/get-project.md) | `GET /projects/{projectId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Get service](actions/get-service.md) | `GET /projects/{projectId}/services/{serviceId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Get service build](actions/get-service-build.md) | `GET /projects/{projectId}/services/{serviceId}/build/{buildId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Job logs](actions/job-logs.md) | `GET /projects/{projectId}/jobs/{jobId}/logs` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List addon types](actions/list-addon-types.md) | `GET /addon-types` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List addons](actions/list-addons.md) | `GET /projects/{projectId}/addons` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List backup destinations](actions/list-backup-destinations.md) | `GET /backup-destinations` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List cloud providers](actions/list-cloud-providers.md) | `GET /cloud-providers` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List domains](actions/list-domains.md) | `GET /domains` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List jobs](actions/list-jobs.md) | `GET /projects/{projectId}/jobs` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List plans](actions/list-plans.md) | `GET /plans` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List projects](actions/list-projects.md) | `GET /projects` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List regions](actions/list-regions.md) | `GET /regions` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List secrets](actions/list-secrets.md) | `GET /secrets` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List services](actions/list-services.md) | `GET /projects/{projectId}/services` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [List tags](actions/list-tags.md) | `GET /tags` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Service logs](actions/service-logs.md) | `GET /projects/{projectId}/services/{serviceId}/logs` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Service metrics](actions/service-metrics.md) | `GET /projects/{projectId}/services/{serviceId}/metrics` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Trigger job run](actions/trigger-job-run.md) | `POST /projects/{projectId}/jobs/{jobId}/runs` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Update job](actions/update-job.md) | `PATCH /projects/{projectId}/jobs/{jobId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
| [Update project](actions/update-project.md) | `PATCH /projects/{projectId}` | [docs](https://northflank.com/docs/v1/api/use-the-api) |
