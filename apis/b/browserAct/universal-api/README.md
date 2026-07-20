# <img src="https://images.mindcloud.co/apps/icons/browser-act_1774977483509.png" alt="BrowserAct logo" width="28" height="28"> BrowserAct: Universal API

Run web scraping and browser automation workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/browserAct/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.browseract.com
- **Vendor API docs:** https://docs.browseract.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Official Workflow Templates](actions/list-official-workflow-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-official-workflow-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Running Task](actions/cancel-running-task.md) | PUT | Updates a running task in BrowserAct to cancel execution. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from BrowserAct. |
| [Resume Paused Task](actions/resume-paused-task.md) | PUT | Updates a paused task in BrowserAct to resume execution. |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a task from BrowserAct. |
| [Retrieve Task Status](actions/retrieve-task-status.md) | GET | Retrieves the current status of a task from BrowserAct. |
| [Run Official Workflow Template](actions/run-official-workflow-template.md) | POST | Creates a new task in BrowserAct from an official workflow template. |
| [Run Workflow](actions/run-workflow.md) | POST | Creates a new task in BrowserAct from a workflow. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Official Workflow Templates](actions/list-official-workflow-templates.md) | GET | Retrieves official workflow templates from BrowserAct. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Official Workflow Template](actions/retrieve-official-workflow-template.md) | GET | Retrieves an official workflow template from BrowserAct. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Proxy Regions](actions/list-supported-proxy-regions.md) | GET | Retrieves supported proxy regions from BrowserAct. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from BrowserAct. |
| [Retrieve Workflow](actions/retrieve-workflow.md) | GET | Retrieves a workflow from BrowserAct. |

