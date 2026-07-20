# Clarifai: Native API Reference

A consolidated summary of Clarifai's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://docs.clarifai.com/resources/api-overview/
- **API base URL:** `https://api.clarifai.com`

## Authentication

### Personal Access Token

Authenticate with a Clarifai personal access token and user ID.

### Credentials

- **API Key:** `apiKey` · required
- **User ID:** `userId` · required · Your Clarifai user ID from Settings > Account.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.clarifai.com/control/authentication/authorize/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Inputs To Dataset](actions/add-inputs-to-dataset.md) | `POST /v2/users/me/apps/:appId/datasets/:datasetId/inputs` | [docs](https://docs.clarifai.com/create/datasets/upload/) |
| [Create Annotations](actions/create-annotations.md) | `POST /v2/annotations` | [docs](https://docs.clarifai.com/create/labeling/api/annotations/) |
| [Create App](actions/create-app.md) | `POST /v2/users/{{credentials.userId}}/apps` | [docs](https://docs.clarifai.com/create/applications/create/) |
| [Create Concept Relations](actions/create-concept-relations.md) | `POST /v2/users/{{credentials.userId}}/apps/{{appId}}/concepts/{{conceptId}}/relations` | [docs](https://docs.clarifai.com/create/concepts/concepts-relations/) |
| [Create Concepts](actions/create-concepts.md) | `POST /v2/users/me/apps/:appId/concepts` | [docs](https://docs.clarifai.com/create/concepts/create/) |
| [Create Concepts by User App ID](actions/create-concepts-by-user-app-id.md) | `POST /v2/concepts` | [docs](https://docs.clarifai.com/create/concepts/create/) |
| [Create Custom Model](actions/create-custom-model.md) | `POST /v2/users/me/apps/:appId/models` | [docs](https://docs.clarifai.com/create/models/) |
| [Create Dataset](actions/create-dataset.md) | `POST /v2/users/me/apps/:appId/datasets` | [docs](https://docs.clarifai.com/create/datasets/create/) |
| [Create Dataset Version](actions/create-dataset-version.md) | `POST /v2/users/me/apps/:appId/datasets/:datasetId/versions` | [docs](https://docs.clarifai.com/create/datasets/create/) |
| [Create Labeling Task](actions/create-labeling-task.md) | `POST /v2/tasks` | [docs](https://docs.clarifai.com/create/labeling/api/tasks/) |
| [Create Visual Classifier Model](actions/create-visual-classifier-model.md) | `POST /v2/models` | [docs](https://docs.clarifai.com/create/models/deep-fine-tuning/visual-classifier/) |
| [Create Workflow](actions/create-workflow.md) | `POST /v2/users/me/apps/:appId/workflows` | [docs](https://docs.clarifai.com/create/workflows/create/) |
| [Delete Annotations](actions/delete-annotations.md) | `DELETE /v2/users/{{credentials.userId}}/apps/{{appId}}/annotations` | [docs](https://docs.clarifai.com/create/labeling/api/annotations-delete/) |
| [Delete Dataset](actions/delete-dataset.md) | `DELETE /v2/users/{{credentials.userId}}/apps/{{appId}}/datasets` | [docs](https://docs.clarifai.com/create/datasets/manage/) |
| [Delete Inputs](actions/delete-inputs.md) | `DELETE /v2/users/{{credentials.userId}}/apps/{{appId}}/inputs` | [docs](https://docs.clarifai.com/create/inputs/manage/) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /v2/users/{{credentials.userId}}/apps/{{appId}}/workflows/{{workflowId}}` | [docs](https://docs.clarifai.com/create/workflows/manage/) |
| [Get Input By ID](actions/get-input-by-id.md) | `GET /v2/users/me/apps/:appId/inputs/:inputId` | [docs](https://docs.clarifai.com/create/inputs/manage/) |
| [Get Labeling Task](actions/get-labeling-task.md) | `GET /v2/users/{{credentials.userId}}/apps/{{appId}}/tasks/{{taskId}}` | [docs](https://docs.clarifai.com/create/labeling/api/tasks/) |
| [Get Workflow By ID](actions/get-workflow-by-id.md) | `GET /v2/users/me/apps/:appId/workflows/:workflowId` | [docs](https://docs.clarifai.com/create/workflows/manage/) |
| [List Annotations](actions/list-annotations.md) | `GET /v2/users/{{credentials.userId}}/apps/{{appId}}/annotations` | [docs](https://docs.clarifai.com/create/labeling/api/annotations-list/) |
| [List Apps](actions/list-apps.md) | `GET /v2/users/{{credentials.userId}}/apps` | [docs](https://docs.clarifai.com/create/applications/manage/) |
| [List Concept Relations](actions/list-concept-relations.md) | `GET /v2/users/{{credentials.userId}}/apps/{{appId}}/concepts/{{conceptId}}/relations` | [docs](https://docs.clarifai.com/create/concepts/concepts-relations/) |
| [List Concepts](actions/list-concepts.md) | `GET /v2/users/me/apps/:appId/concepts` | [docs](https://docs.clarifai.com/create/concepts/manage/) |
| [List Dataset Versions](actions/list-dataset-versions.md) | `GET /v2/users/me/apps/:appId/datasets/:datasetId/versions` | [docs](https://docs.clarifai.com/create/datasets/manage/) |
| [List Datasets](actions/list-datasets.md) | `GET /v2/users/me/apps/:appId/datasets` | [docs](https://docs.clarifai.com/create/datasets/manage/) |
| [List Inputs](actions/list-inputs.md) | `GET /v2/users/me/apps/:appId/inputs` | [docs](https://docs.clarifai.com/create/inputs/manage/) |
| [List Labeling Tasks](actions/list-labeling-tasks.md) | `GET /v2/users/{{credentials.userId}}/apps/{{appId}}/tasks` | [docs](https://docs.clarifai.com/create/labeling/api/tasks/) |
| [List Model Concepts](actions/list-model-concepts.md) | `GET /v2/users/me/apps/:appId/models/:modelId/concepts` | [docs](https://docs.clarifai.com/create/models/manage/) |
| [List Model Versions](actions/list-model-versions.md) | `GET /v2/users/me/apps/:appId/models/:modelId/versions` | [docs](https://docs.clarifai.com/create/models/model-versions/) |
| [List Models](actions/list-models.md) | `GET /v2/users/me/apps/:appId/models` | [docs](https://docs.clarifai.com/create/models/manage/) |
| [List Public Models](actions/list-public-models.md) | `GET /v2/users/clarifai/apps/main/models` | [docs](https://docs.clarifai.com/create/models/manage/) |
| [List Workflows](actions/list-workflows.md) | `GET /v2/users/me/apps/:appId/workflows` | [docs](https://docs.clarifai.com/create/workflows/manage/) |
| [Search Models](actions/search-models.md) | `POST /v2/users/me/apps/:appId/models/searches` | [docs](https://docs.clarifai.com/create/models/manage/) |
| [Update Annotations](actions/update-annotations.md) | `PATCH /v2/annotations` | [docs](https://docs.clarifai.com/create/labeling/api/annotations-update/) |
| [Update Concept](actions/update-concept.md) | `PATCH /v2/concepts` | [docs](https://docs.clarifai.com/create/concepts/manage/) |
| [Update Dataset](actions/update-dataset.md) | `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/datasets` | [docs](https://docs.clarifai.com/create/datasets/manage/) |
| [Update Dataset Version](actions/update-dataset-version.md) | `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/datasets/{{datasetId}}/versions` | [docs](https://docs.clarifai.com/create/datasets/manage/) |
| [Update Labeling Task](actions/update-labeling-task.md) | `PATCH /v2/tasks` | [docs](https://docs.clarifai.com/create/labeling/api/tasks/) |
| [Update Model Metadata](actions/update-model-metadata.md) | `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/models` | [docs](https://docs.clarifai.com/create/models/manage/) |
| [Update Workflow](actions/update-workflow.md) | `PATCH /v2/users/{{credentials.userId}}/apps/{{appId}}/workflows` | [docs](https://docs.clarifai.com/create/workflows/manage/) |
| [Upload Inputs](actions/upload-inputs.md) | `POST /v2/users/me/apps/:appId/inputs` | [docs](https://docs.clarifai.com/create/inputs/upload/api/) |
