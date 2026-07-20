# <img src="https://images.mindcloud.co/apps/icons/airiam-ai_1775853694832.png" alt="Airiam AI logo" width="28" height="28"> Airiam AI: Universal API

Use Airiam AI to manage workspaces, models, AI experts, and chat workflows from the Airiam REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airiamAI/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ai.airiam.com
- **Vendor API docs:** https://docs.ai.airiam.com/reference/getting-started-with-the-airiam-ai-restapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Chat Thread

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat History](actions/get-chat-history.md) | GET | Retrieves chat history for a workspace in Airiam AI. |

### Expert

| Action | Method | Description |
| --- | --- | --- |
| [Create Expert](actions/create-expert.md) | POST | Creates or updates an expert in Airiam AI. |
| [Delete Expert](actions/delete-expert.md) | DELETE | Deletes an existing expert from Airiam AI. |
| [Get Expert](actions/get-expert.md) | GET | Retrieves an expert from Airiam AI. |
| [List Experts](actions/list-experts.md) | GET | Retrieves a list of experts from Airiam AI. |

### Expert File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Expert File](actions/delete-expert-file.md) | DELETE | Deletes an existing expert file from Airiam AI. |
| [Get Expert File Content](actions/get-expert-file-content.md) | GET | Retrieves expert file content from Airiam AI. |

### Greeting

| Action | Method | Description |
| --- | --- | --- |
| [Get Greeting](actions/get-greeting.md) | GET | Retrieves the greeting for a workspace in Airiam AI. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Add Model To Team](actions/add-model-to-team.md) | PUT | Adds a model to the team in Airiam AI. |
| [Create Model](actions/create-model.md) | POST | Creates a new model in Airiam AI. |
| [Get All Models](actions/get-all-models.md) | GET | Retrieves all models from Airiam AI. |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from Airiam AI by model ID. |
| [List All Models With Body](actions/list-all-models-post.md) | GET | Retrieves all active models from Airiam AI by model IDs. |
| [List Models](actions/list-models.md) | GET | Retrieves a list of models from Airiam AI. |
| [List Models With Body](actions/list-models-post.md) | GET | Retrieves active models from Airiam AI by model IDs. |
| [Remove Model From Team](actions/remove-model-from-team.md) | PUT | Removes a model from the team in Airiam AI. |
| [Update Model](actions/update-model.md) | PUT | Updates an existing model in Airiam AI. |

### Sample Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Get Sample Prompts](actions/get-sample-prompts.md) | GET | Retrieves sample prompts for a workspace in Airiam AI. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Airiam AI. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from Airiam AI. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Airiam AI. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves a list of workspaces from Airiam AI. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Airiam AI. |
| [Update Workspace Model](actions/update-workspace-model.md) | PUT | Updates a workspace model in Airiam AI. |

