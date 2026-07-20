# <img src="https://images.mindcloud.co/apps/icons/braintrust_1778179767817.png" alt="Braintrust logo" width="28" height="28"> Braintrust: Universal API

Evaluate, monitor, and manage AI product data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/braintrust/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.braintrust.dev
- **Vendor API docs:** https://www.braintrust.dev/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintrust/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Cross Object Insert

| Action | Method | Description |
| --- | --- | --- |
| [Cross Object Insert](actions/cross-object-insert.md) | POST | Inserts events and feedback across Braintrust objects. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a new dataset in Braintrust. |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from Braintrust. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from Braintrust. |

### Dataset Event

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Dataset](actions/fetch-dataset.md) | GET | Retrieves events from a dataset in Braintrust. |
| [Insert Dataset Events](actions/insert-dataset-events.md) | POST | Creates dataset events in Braintrust. |

### Dataset Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Feedback For Dataset Events](actions/feedback-for-dataset-events.md) | POST | Creates feedback for dataset events in Braintrust. |

### Dataset Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Dataset](actions/summarize-dataset.md) | GET | Retrieves a summary of a dataset in Braintrust. |

### Eval

| Action | Method | Description |
| --- | --- | --- |
| [Launch Eval](actions/launch-eval.md) | POST | Launches an eval in Braintrust. |

### Experiment

| Action | Method | Description |
| --- | --- | --- |
| [Create Experiment](actions/create-experiment.md) | POST | Creates a new experiment in Braintrust. |
| [Get Experiment](actions/get-experiment.md) | GET | Retrieves an experiment from Braintrust. |
| [List Experiments](actions/list-experiments.md) | GET | Retrieves experiments from Braintrust. |

### Experiment Event

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Experiment](actions/fetch-experiment.md) | GET | Retrieves events from an experiment in Braintrust. |
| [Insert Experiment Events](actions/insert-experiment-events.md) | POST | Creates experiment events in Braintrust. |

### Experiment Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Feedback For Experiment Events](actions/feedback-for-experiment-events.md) | POST | Creates feedback for experiment events in Braintrust. |

### Experiment Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Experiment](actions/summarize-experiment.md) | GET | Retrieves a summary of an experiment in Braintrust. |

### Function

| Action | Method | Description |
| --- | --- | --- |
| [Create Function](actions/create-function.md) | POST | Creates a new function in Braintrust. |
| [Get Function](actions/get-function.md) | GET | Retrieves a function from Braintrust. |
| [List Functions](actions/list-functions.md) | GET | Retrieves functions from Braintrust. |
| [Update Function](actions/update-function.md) | PUT | Updates an existing function in Braintrust. |

### Function Invocation

| Action | Method | Description |
| --- | --- | --- |
| [Invoke Function](actions/invoke-function.md) | POST | Invokes a function in Braintrust. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Braintrust. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Braintrust. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Braintrust. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Braintrust. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Braintrust. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Braintrust. |

### Project Log

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Project Logs](actions/fetch-project-logs.md) | GET | Retrieves events from project logs in Braintrust. |

### Project Log Event

| Action | Method | Description |
| --- | --- | --- |
| [Insert Project Logs Events](actions/insert-project-logs-events.md) | POST | Creates project log events in Braintrust. |

### Project Log Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Feedback For Project Logs](actions/feedback-for-project-logs.md) | POST | Creates feedback for project log events in Braintrust. |

### Project Score

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Score](actions/create-project-score.md) | POST | Creates a new project score in Braintrust. |
| [List Project Scores](actions/list-project-scores.md) | GET | Retrieves project scores from Braintrust. |

### Project Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Tag](actions/create-project-tag.md) | POST | Creates a new project tag in Braintrust. |
| [List Project Tags](actions/list-project-tags.md) | GET | Retrieves project tags from Braintrust. |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt.md) | POST | Creates a new prompt in Braintrust. |
| [Get Prompt](actions/get-prompt.md) | GET | Retrieves a prompt from Braintrust. |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves prompts from Braintrust. |
| [Update Prompt](actions/update-prompt.md) | PUT | Updates an existing prompt in Braintrust. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Braintrust. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Views](actions/list-views.md) | GET | Retrieves views from Braintrust. |

