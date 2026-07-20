# <img src="https://images.mindcloud.co/apps/icons/images-4_1775073619651.png" alt="Arize AX logo" width="28" height="28"> Arize AX: Universal API

Arize AX is a unified AI engineering platform for prompts, tracing, evaluation, experimentation, and production monitoring across LLM and agent applications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/arizeAX/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://arize.com
- **Vendor API docs:** https://arize.com/docs/ax/rest-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Spaces](actions/list-spaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Add New Examples To A Dataset](actions/add-new-examples-to-a-dataset.md) | PUT | Adds new examples to an existing dataset in Arize AX. |
| [Create a Dataset](actions/create-a-dataset.md) | POST | Creates a new dataset in Arize AX. |
| [Get a Dataset](actions/get-a-dataset.md) | GET | Retrieves a dataset from Arize AX. |
| [List Dataset Examples](actions/list-dataset-examples.md) | GET | Retrieves examples for a dataset in Arize AX. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from Arize AX. |
| [Update Existing Examples In A Dataset](actions/update-existing-examples-in-a-dataset.md) | PUT | Updates existing examples in a dataset in Arize AX. |

### Experiments

| Action | Method | Description |
| --- | --- | --- |
| [Create an Experiment](actions/create-an-experiment.md) | POST | Creates a new experiment in Arize AX. |
| [Get an Experiment](actions/get-an-experiment.md) | GET | Retrieves an experiment from Arize AX. |
| [List Experiment Runs](actions/list-experiment-runs.md) | GET | Retrieves runs for an experiment in Arize AX. |
| [List Experiments](actions/list-experiments.md) | GET | Retrieves experiments from Arize AX. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create a Project](actions/create-a-project.md) | POST | Creates a new project in Arize AX. |
| [Get a Project](actions/get-a-project.md) | GET | Retrieves a project from Arize AX. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Arize AX. |

### Scorecards

| Action | Method | Description |
| --- | --- | --- |
| [Create Evaluator](actions/create-evaluator.md) | POST | Creates a new evaluator in Arize AX. |
| [Create Evaluator Version](actions/create-evaluator-version.md) | POST | Creates a new evaluator version in Arize AX. |
| [Get Evaluator](actions/get-evaluator.md) | GET | Retrieves an evaluator from Arize AX. |
| [Get Evaluator Version](actions/get-evaluator-version.md) | GET | Retrieves an evaluator version from Arize AX. |
| [List Evaluator Versions](actions/list-evaluator-versions.md) | GET | Retrieves versions for an evaluator in Arize AX. |
| [List Evaluators](actions/list-evaluators.md) | GET | Retrieves evaluators from Arize AX. |
| [Update Evaluator](actions/update-evaluator.md) | PUT | Updates an evaluator in Arize AX. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create a Prompt](actions/create-a-prompt.md) | POST | Creates a new prompt in Arize AX. |
| [Create a Prompt Version](actions/create-a-prompt-version.md) | POST | Creates a new prompt version in Arize AX. |
| [Get a Prompt](actions/get-a-prompt.md) | GET | Retrieves a prompt from Arize AX. |
| [Get a Prompt Version](actions/get-a-prompt-version.md) | GET | Retrieves a prompt version from Arize AX. |
| [List Prompt Versions](actions/list-prompt-versions.md) | GET | Retrieves versions for a prompt in Arize AX. |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves prompts from Arize AX. |
| [Update a Prompt](actions/update-a-prompt.md) | PUT | Updates a prompt in Arize AX. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Spans](actions/list-spans.md) | GET | Retrieves spans from Arize AX. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get a Space](actions/get-a-space.md) | GET | Retrieves a space from Arize AX. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from Arize AX. |

