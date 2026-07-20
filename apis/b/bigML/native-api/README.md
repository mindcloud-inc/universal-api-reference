# BigML: Native API Reference

A consolidated summary of BigML's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://bigml.com/api/
- **API base URL:** `https://bigml.io`

## Authentication

### API Key (Query)

BigML query-parameter authentication using username and API key.

### Credentials

- **API Key:** `apiKey` · required
- **BigML Username (not email):** `username` · required · Use the BigML username shown in the dashboard account area, not your login email address.
- **Project ID:** `projectId` · optional · Optional BigML project ID for organization workspace access.
- **Organization ID:** `organizationId` · optional · Optional BigML organization ID when required by workspace context.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.bigml.com/hc/en-us/articles/206616689-Where-can-I-find-my-username-and-my-API-Key)

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | `POST /dataset` | [docs](https://bigml.com/api/) |
| [Create Model](actions/create-model.md) | `POST /model` | [docs](https://bigml.com/api/) |
| [Create Prediction](actions/create-prediction.md) | `POST /prediction` | [docs](https://bigml.com/api/) |
| [Create Source](actions/create-source.md) | `POST /source` | [docs](https://bigml.com/api/) |
| [Get Anomaly](actions/get-anomaly.md) | `GET /anomaly/:anomalyId` | [docs](https://bigml.com/api/) |
| [Get Batch Prediction](actions/get-batch-prediction.md) | `GET /batchprediction/:batchPredictionId` | [docs](https://bigml.com/api/) |
| [Get Cluster](actions/get-cluster.md) | `GET /cluster/:clusterId` | [docs](https://bigml.com/api/) |
| [Get Dataset](actions/get-dataset.md) | `GET /dataset/:datasetId` | [docs](https://bigml.com/api/) |
| [Get Ensemble](actions/get-ensemble.md) | `GET /ensemble/:ensembleId` | [docs](https://bigml.com/api/) |
| [Get Evaluation](actions/get-evaluation.md) | `GET /evaluation/:evaluationId` | [docs](https://bigml.com/api/) |
| [Get Model](actions/get-model.md) | `GET /model/:modelId` | [docs](https://bigml.com/api/) |
| [Get Prediction](actions/get-prediction.md) | `GET /prediction/:predictionId` | [docs](https://bigml.com/api/) |
| [Get Project](actions/get-project.md) | `GET /project/:projectId` | [docs](https://bigml.com/api/) |
| [Get Source](actions/get-source.md) | `GET /source/:sourceId` | [docs](https://bigml.com/api/) |
| [List Anomalies](actions/list-anomalies.md) | `GET /anomaly` | [docs](https://bigml.com/api/) |
| [List Batch Predictions](actions/list-batch-predictions.md) | `GET /batchprediction` | [docs](https://bigml.com/api/) |
| [List Clusters](actions/list-clusters.md) | `GET /cluster` | [docs](https://bigml.com/api/) |
| [List Datasets](actions/list-datasets.md) | `GET /dataset` | [docs](https://bigml.com/api/) |
| [List Ensembles](actions/list-ensembles.md) | `GET /ensemble` | [docs](https://bigml.com/api/) |
| [List Evaluations](actions/list-evaluations.md) | `GET /evaluation` | [docs](https://bigml.com/api/) |
| [List Models](actions/list-models.md) | `GET /model` | [docs](https://bigml.com/api/) |
| [List Predictions](actions/list-predictions.md) | `GET /prediction` | [docs](https://bigml.com/api/) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://bigml.com/api/) |
| [List Sources](actions/list-sources.md) | `GET /source` | [docs](https://bigml.com/api/) |
