# <img src="https://images.mindcloud.co/apps/icons/ui-path-orchestrator_1778005544364.png" alt="UiPath Orchestrator logo" width="28" height="28"> UiPath Orchestrator: Universal API

UiPath Orchestrator manages automation folders, assets, queues, jobs, robots, machines, tasks, processes, schedules, and related operational resources through UiPath Automation Cloud APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uiPathOrchestrator/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.uipath.com/product/orchestrator
- **Vendor API docs:** https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get asset](actions/get-asset.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-asset?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Create asset](actions/create-asset.md) | POST |  |
| [Delete asset](actions/delete-asset.md) | DELETE |  |
| [Get asset](actions/get-asset.md) | GET |  |
| [List assets](actions/list-assets.md) | GET |  |
| [Update asset](actions/update-asset.md) | PUT |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get folder](actions/get-folder.md) | GET |  |
| [List folders](actions/list-folders.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get job](actions/get-job.md) | GET |  |
| [List jobs](actions/list-jobs.md) | GET |  |
| [Start jobs](actions/start-jobs.md) | POST |  |
| [Stop job](actions/stop-job.md) | PUT |  |

### Machine

| Action | Method | Description |
| --- | --- | --- |
| [Get machine](actions/get-machine.md) | GET |  |
| [List machines](actions/list-machines.md) | GET |  |

### Process

| Action | Method | Description |
| --- | --- | --- |
| [Get process](actions/get-process.md) | GET |  |
| [List processes](actions/list-processes.md) | GET |  |

### Queue

| Action | Method | Description |
| --- | --- | --- |
| [Create queue](actions/create-queue.md) | POST |  |
| [Get queue](actions/get-queue.md) | GET |  |
| [List queues](actions/list-queues.md) | GET |  |

### Queue Item

| Action | Method | Description |
| --- | --- | --- |
| [Get queue item](actions/get-queue-item.md) | GET |  |
| [List queue items](actions/list-queue-items.md) | GET |  |

### Robot

| Action | Method | Description |
| --- | --- | --- |
| [Get robot](actions/get-robot.md) | GET |  |
| [List robots](actions/list-robots.md) | GET |  |

### Runtime License

| Action | Method | Description |
| --- | --- | --- |
| [List runtime licenses](actions/list-runtime-licenses.md) | GET |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get schedule](actions/get-schedule.md) | GET |  |
| [List schedules](actions/list-schedules.md) | GET |  |

### Setting

| Action | Method | Description |
| --- | --- | --- |
| [List settings](actions/list-settings.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get task](actions/get-task.md) | GET |  |
| [List tasks across folders](actions/list-tasks-across-folders.md) | GET |  |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [List tenants](actions/list-tenants.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List users](actions/list-users.md) | GET |  |

