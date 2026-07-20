# <img src="https://images.mindcloud.co/apps/icons/big-ml_1775066468875.png" alt="BigML logo" width="28" height="28"> BigML: Universal API

BigML is a machine learning platform for creating datasets, models, and predictions through a REST API and dashboard.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bigML/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bigml.com/
- **Vendor API docs:** https://bigml.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sources](actions/list-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigML/latest/actions/list-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Anomaly

| Action | Method | Description |
| --- | --- | --- |
| [Get Anomaly](actions/get-anomaly.md) | GET | Retrieves an anomaly detector from BigML. |
| [List Anomalies](actions/list-anomalies.md) | GET | Retrieves anomaly detectors from BigML. |

### Cluster

| Action | Method | Description |
| --- | --- | --- |
| [Get Cluster](actions/get-cluster.md) | GET | Retrieves a cluster from BigML. |
| [List Clusters](actions/list-clusters.md) | GET | Retrieves clusters from BigML. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a dataset in BigML. |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from BigML. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from BigML. |

### Ensemble

| Action | Method | Description |
| --- | --- | --- |
| [Get Ensemble](actions/get-ensemble.md) | GET | Retrieves an ensemble from BigML. |
| [List Ensembles](actions/list-ensembles.md) | GET | Retrieves ensembles from BigML. |

### Evaluation

| Action | Method | Description |
| --- | --- | --- |
| [Get Evaluation](actions/get-evaluation.md) | GET | Retrieves an evaluation from BigML. |
| [List Evaluations](actions/list-evaluations.md) | GET | Retrieves evaluations from BigML. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a model in BigML. |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from BigML. |
| [List Models](actions/list-models.md) | GET | Retrieves models from BigML. |

### Prediction

| Action | Method | Description |
| --- | --- | --- |
| [Create Prediction](actions/create-prediction.md) | POST | Creates a prediction in BigML. |
| [Get Batch Prediction](actions/get-batch-prediction.md) | GET | Retrieves a batch prediction from BigML. |
| [Get Prediction](actions/get-prediction.md) | GET | Retrieves a prediction from BigML. |
| [List Batch Predictions](actions/list-batch-predictions.md) | GET | Retrieves batch predictions from BigML. |
| [List Predictions](actions/list-predictions.md) | GET | Retrieves predictions from BigML. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from BigML. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from BigML. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a source in BigML. |
| [Get Source](actions/get-source.md) | GET | Retrieves a source from BigML. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from BigML. |

