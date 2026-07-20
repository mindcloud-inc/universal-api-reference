# <img src="https://images.mindcloud.co/apps/icons/skyvern_1773833568722.png" alt="Skyvern logo" width="28" height="28"> Skyvern: Universal API

Run browser tasks, workflows, and scripts with Skyvern

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/skyvern/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.skyvern.com
- **Vendor API docs:** https://www.skyvern.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Folders](actions/list-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/list-folders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Artifact

| Action | Method | Description |
| --- | --- | --- |
| [Get Artifact](actions/get-artifact.md) | GET | Retrieves a run artifact from Skyvern. |
| [List Run Artifacts](actions/list-run-artifacts.md) | GET | Retrieves artifacts for a run from Skyvern. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new workflow folder in Skyvern. |
| [List Folders](actions/list-folders.md) | GET | Retrieves workflow folders for your organization from Skyvern. |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | PUT | Cancels a task or workflow run in Skyvern. |
| [Get Run](actions/get-run.md) | GET | Retrieves task or workflow run details from Skyvern. |
| [Retry Run Webhook](actions/retry-run-webhook.md) | PUT | Retries webhook delivery for a run in Skyvern. |

### Runtimeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Run Timeline](actions/get-run-timeline.md) | GET | Retrieves timeline events for a run from Skyvern. |

### Script

| Action | Method | Description |
| --- | --- | --- |
| [Create Script](actions/create-script.md) | POST | Creates a new script in Skyvern. |
| [Get Script](actions/get-script.md) | GET | Retrieves a script by ID from Skyvern. |

### Taskrun

| Action | Method | Description |
| --- | --- | --- |
| [Run File Download Task](actions/run-file-download-task.md) | POST | Runs a file download task in Skyvern. |
| [Run Login Task](actions/run-login-task.md) | POST | Runs a login automation task in Skyvern. |
| [Run Task](actions/run-task.md) | POST | Runs a browser automation task in Skyvern. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in Skyvern. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes an existing workflow from Skyvern. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow by permanent ID from Skyvern. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows and their latest versions from Skyvern. |
| [Update Workflow](actions/update-workflow.md) | PUT | Updates an existing workflow in Skyvern. |
| [Update Workflow Folder](actions/update-workflow-folder.md) | PUT | Updates a workflow's folder assignment in Skyvern. |

### Workflowrun

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Runs](actions/list-workflow-runs.md) | GET | Retrieves workflow runs for your organization from Skyvern. |
| [Run Workflow](actions/run-workflow.md) | POST | Runs a workflow in Skyvern. |

### Workflowversion

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Versions](actions/list-workflow-versions.md) | GET | Retrieves all versions of a workflow from Skyvern. |

