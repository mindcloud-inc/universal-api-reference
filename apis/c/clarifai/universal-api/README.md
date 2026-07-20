# <img src="https://images.mindcloud.co/apps/icons/clarifai_1775156826866.png" alt="Clarifai logo" width="28" height="28"> Clarifai: Universal API

Build, deploy, and manage AI models, workflows, and data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clarifai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clarifai.com
- **Vendor API docs:** https://docs.clarifai.com/resources/api-overview/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Public Models](actions/list-public-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-public-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create App](actions/create-app.md) | POST | Creates a new app in Clarifai. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from Clarifai. |

### Concept

| Action | Method | Description |
| --- | --- | --- |
| [Create Concepts](actions/create-concepts.md) | POST | Creates concepts in Clarifai. |
| [List Concepts](actions/list-concepts.md) | GET | Retrieves concepts from Clarifai. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a new dataset in Clarifai. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from Clarifai. |

### Dataset Input

| Action | Method | Description |
| --- | --- | --- |
| [Add Inputs To Dataset](actions/add-inputs-to-dataset.md) | PUT | Adds inputs to a dataset in Clarifai. |

### Dataset Version

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset Version](actions/create-dataset-version.md) | POST | Creates a dataset version in Clarifai. |
| [List Dataset Versions](actions/list-dataset-versions.md) | GET | Retrieves dataset versions from Clarifai. |

### Input

| Action | Method | Description |
| --- | --- | --- |
| [Get Input By ID](actions/get-input-by-id.md) | GET | Retrieves an input from Clarifai. |
| [List Inputs](actions/list-inputs.md) | GET | Retrieves inputs from Clarifai. |
| [Upload Inputs](actions/upload-inputs.md) | POST | Uploads inputs to an app in Clarifai. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Visual Classifier Model](actions/create-visual-classifier-model.md) | POST | Creates a visual classifier model in Clarifai. |
| [List Public Models](actions/list-public-models.md) | GET | Retrieves public models from Clarifai. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Model Concepts](actions/list-model-concepts.md) | GET | Retrieves model concepts from Clarifai. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotations](actions/create-annotations.md) | POST | Creates annotations in Clarifai. |
| [Create Concept Relations](actions/create-concept-relations.md) | POST | Creates concept relations in Clarifai. |
| [Create Concepts by User App ID](actions/create-concepts-by-user-app-id.md) | POST | Creates concepts in Clarifai. |
| [Create Custom Model](actions/create-custom-model.md) | POST | Creates a custom model in Clarifai. |
| [Create Labeling Task](actions/create-labeling-task.md) | POST | Creates a labeling task in Clarifai. |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in Clarifai. |
| [Delete Annotations](actions/delete-annotations.md) | DELETE | Deletes existing annotations from Clarifai. |
| [Delete Dataset](actions/delete-dataset.md) | DELETE | Deletes an existing dataset from Clarifai. |
| [Delete Inputs](actions/delete-inputs.md) | DELETE | Deletes existing inputs from Clarifai. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes an existing workflow from Clarifai. |
| [Get Labeling Task](actions/get-labeling-task.md) | GET | Retrieves a labeling task from Clarifai. |
| [Get Workflow By ID](actions/get-workflow-by-id.md) | GET | Retrieves a workflow from Clarifai. |
| [List Annotations](actions/list-annotations.md) | GET | Retrieves annotations from Clarifai. |
| [List Concept Relations](actions/list-concept-relations.md) | GET | Retrieves concept relations from Clarifai. |
| [List Labeling Tasks](actions/list-labeling-tasks.md) | GET | Retrieves labeling tasks from Clarifai. |
| [List Model Versions](actions/list-model-versions.md) | GET | Retrieves model versions from Clarifai. |
| [List Models](actions/list-models.md) | GET | Retrieves models from Clarifai. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Clarifai. |
| [Search Models](actions/search-models.md) | GET | Finds models in Clarifai by model ID or name. |
| [Update Annotations](actions/update-annotations.md) | PATCH | Updates existing annotations in Clarifai. |
| [Update Concept](actions/update-concept.md) | PATCH | Updates an existing concept in Clarifai. |
| [Update Dataset](actions/update-dataset.md) | PATCH | Updates an existing dataset in Clarifai. |
| [Update Dataset Version](actions/update-dataset-version.md) | PATCH | Updates an existing dataset version in Clarifai. |
| [Update Labeling Task](actions/update-labeling-task.md) | PATCH | Updates an existing labeling task in Clarifai. |
| [Update Model Metadata](actions/update-model-metadata.md) | PATCH | Updates existing model metadata in Clarifai. |
| [Update Workflow](actions/update-workflow.md) | PATCH | Updates an existing workflow in Clarifai. |

