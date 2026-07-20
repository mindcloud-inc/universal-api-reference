# <img src="https://images.mindcloud.co/apps/icons/honey-hive_1776177635296.png" alt="HoneyHive logo" width="28" height="28"> HoneyHive: Universal API

HoneyHive is an AI observability and evaluation platform for tracing sessions/events, managing datasets, metrics, tools, projects, experiment runs, and configurations through the HoneyHive API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/honeyHive/latest
- **Category:** IT Operations / Observability
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://honeyhive.ai
- **Vendor API docs:** https://docs.honeyhive.ai/sdk-reference/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Projects](actions/get-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Create Configuration](actions/create-configuration.md) | POST | Creates a new configuration in HoneyHive. |
| [Delete Configuration](actions/delete-configuration.md) | DELETE | Deletes an existing configuration from HoneyHive. |
| [Get Configurations](actions/get-configurations.md) | GET | Retrieves a list of configurations from HoneyHive. |
| [Update Configuration](actions/update-configuration.md) | PUT | Updates an existing configuration in HoneyHive. |

### Datapoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Datapoint](actions/create-datapoint.md) | POST | Creates a new datapoint in HoneyHive. |
| [Delete Datapoint](actions/delete-datapoint.md) | DELETE | Deletes an existing datapoint from HoneyHive. |
| [Get Datapoint](actions/get-datapoint.md) | GET | Retrieves a datapoint record from HoneyHive. |
| [Get Datapoints](actions/get-datapoints.md) | GET | Retrieves a list of datapoints from HoneyHive. |
| [Update Datapoint](actions/update-datapoint.md) | PUT | Updates an existing datapoint in HoneyHive. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a new dataset in HoneyHive. |
| [Delete Dataset](actions/delete-dataset.md) | DELETE | Deletes an existing dataset from HoneyHive. |
| [Get Datasets](actions/get-datasets.md) | GET | Retrieves a list of datasets from HoneyHive. |
| [Update Dataset](actions/update-dataset.md) | PUT | Updates an existing dataset in HoneyHive. |

### Dataset Datapoints

| Action | Method | Description |
| --- | --- | --- |
| [Add Datapoints](actions/add-datapoints.md) | POST | Adds datapoints to a dataset in HoneyHive. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in HoneyHive. |
| [Get Events](actions/get-events.md) | GET | Finds events in HoneyHive by filter criteria. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in HoneyHive. |

### Event Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Batch](actions/create-event-batch.md) | POST | Creates a batch of events in HoneyHive. |

### Experiment Comparison

| Action | Method | Description |
| --- | --- | --- |
| [Get Experiment Comparison](actions/get-experiment-comparison.md) | GET | Retrieves an experiment comparison from HoneyHive. |

### Experiment Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Experiment Result](actions/get-experiment-result.md) | GET | Retrieves an experiment result from HoneyHive. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Create Metric](actions/create-metric.md) | POST | Creates a new metric in HoneyHive. |
| [Delete Metric](actions/delete-metric.md) | DELETE | Deletes an existing metric from HoneyHive. |
| [Get Metrics](actions/get-metrics.md) | GET | Retrieves a list of metrics from HoneyHive. |
| [Update Metric](actions/update-metric.md) | PUT | Updates an existing metric in HoneyHive. |

### Model Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Model Event](actions/create-model-event.md) | POST | Creates a new model event in HoneyHive. |

### Model Event Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Model Event Batch](actions/create-model-event-batch.md) | POST | Creates a batch of model events in HoneyHive. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in HoneyHive. |
| [Get Projects](actions/get-projects.md) | GET | Retrieves a list of projects from HoneyHive. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in HoneyHive. |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Create Run](actions/create-run.md) | POST | Creates a new evaluation run in HoneyHive. |
| [Delete Run](actions/delete-run.md) | DELETE | Deletes an evaluation run from HoneyHive. |
| [Get Run](actions/get-run.md) | GET | Retrieves an evaluation run from HoneyHive. |
| [Get Runs](actions/get-runs.md) | GET | Retrieves a list of evaluation runs from HoneyHive. |
| [Update Run](actions/update-run.md) | PUT | Updates an evaluation run in HoneyHive. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET | Retrieves an existing session from HoneyHive. |
| [Start Session](actions/start-session.md) | POST | Creates a new session in HoneyHive. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create Tool](actions/create-tool.md) | POST | Creates a new tool in HoneyHive. |
| [Delete Tool](actions/delete-tool.md) | DELETE | Deletes an existing tool from HoneyHive. |
| [Get Tools](actions/get-tools.md) | GET | Retrieves a list of tools from HoneyHive. |
| [Update Tool](actions/update-tool.md) | PUT | Updates an existing tool in HoneyHive. |

