# Datarobot: Native API Reference

A consolidated summary of Datarobot's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.datarobot.com/en/docs/api/reference/index.html
- **OpenAPI specification:** https://app.datarobot.com/api/v2/openapi.yaml
- **API base URL:** `https://app.datarobot.com/api/v2`

## Authentication

### API Key

Authenticate with a DataRobot API key. DataRobot uses API keys as the preferred authentication method for API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.datarobot.com/en/docs/platform/acct-settings/api-key-mgmt.html)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `orderBy` in the query string. Only one sort field is accepted.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Custom Model](actions/get-custom-model.md) | `GET /customModels/:customModelId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Custom Model Version](actions/get-custom-model-version.md) | `GET /customModels/:customModelId/versions/:customModelVersionId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Dataset](actions/get-dataset.md) | `GET /datasets/:datasetId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Dataset Version](actions/get-dataset-version.md) | `GET /datasets/:datasetId/versions/:datasetVersionId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Deployment](actions/get-deployment.md) | `GET /deployments/:deploymentId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Deployment Agent Card](actions/get-deployment-agent-card.md) | `GET /deployments/:deploymentId/agentCard/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Project Status](actions/get-project-status.md) | `GET /projects/:projectId/status/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Registered Model](actions/get-registered-model.md) | `GET /registeredModels/:registeredModelId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Registered Model Version](actions/get-registered-model-version.md) | `GET /registeredModels/:registeredModelId/versions/:versionId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Use Case](actions/get-use-case.md) | `GET /useCases/:useCaseId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [Get Use Case Dataset](actions/get-use-case-dataset.md) | `GET /useCases/:useCaseId/datasets/:datasetId/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Custom Model Versions](actions/list-custom-model-versions.md) | `GET /customModels/:customModelId/versions/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Custom Models](actions/list-custom-models.md) | `GET /customModels/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Dataset Projects](actions/list-dataset-projects.md) | `GET /datasets/:datasetId/projects/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Dataset Versions](actions/list-dataset-versions.md) | `GET /datasets/:datasetId/versions/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Datasets](actions/list-datasets.md) | `GET /datasets/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Deployment Capabilities](actions/list-deployment-capabilities.md) | `GET /deployments/:deploymentId/capabilities/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Deployment Challengers](actions/list-deployment-challengers.md) | `GET /deployments/:deploymentId/challengers/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Deployment Custom Metrics](actions/list-deployment-custom-metrics.md) | `GET /deployments/:deploymentId/customMetrics/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Deployments](actions/list-deployments.md) | `GET /deployments/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Project Models](actions/list-project-models.md) | `GET /projects/:projectId/models/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Projects](actions/list-projects.md) | `GET /projects/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Registered Model Deployments](actions/list-registered-model-deployments.md) | `GET /registeredModels/:registeredModelId/deployments/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Registered Model Version Deployments](actions/list-registered-model-version-deployments.md) | `GET /registeredModels/:registeredModelId/versions/:versionId/deployments/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Registered Model Versions](actions/list-registered-model-versions.md) | `GET /registeredModels/:registeredModelId/versions/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Registered Models](actions/list-registered-models.md) | `GET /registeredModels/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Use Case Datasets](actions/list-use-case-datasets.md) | `GET /useCases/:useCaseId/datasets/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Use Case Deployments](actions/list-use-case-deployments.md) | `GET /useCases/:useCaseId/deployments/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Use Case Projects](actions/list-use-case-projects.md) | `GET /useCases/:useCaseId/projects/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Use Case Registered Models](actions/list-use-case-registered-models.md) | `GET /useCases/:useCaseId/registeredModels/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
| [List Use Cases](actions/list-use-cases.md) | `GET /useCases/` | [docs](https://docs.datarobot.com/en/docs/api/reference/index.html) |
