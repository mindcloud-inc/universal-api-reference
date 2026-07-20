# <img src="https://images.mindcloud.co/apps/icons/wodely_1774628408923.png" alt="Wodely logo" width="28" height="28"> Wodely: Universal API

Manage last-mile delivery operations and commerce order integrations with Wodely

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wodely/latest
- **Category:** Commerce
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wodely.com/
- **Vendor API docs:** https://app.wodely.com/doc/api-documentation.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Drivers](actions/list-drivers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-drivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Ping API](actions/ping-api.md) | GET |  |

### Driver

| Action | Method | Description |
| --- | --- | --- |
| [List Drivers](actions/list-drivers.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create GloriaFood Job](actions/create-gloriafood-job.md) | POST |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create CloudWaitress Order](actions/create-cloudwaitress-order.md) | POST |  |
| [Create Yelo Order](actions/create-yelo-order.md) | POST |  |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Search Routes](actions/search-routes.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Assign Tasks to Driver in Batch](actions/assign-tasks-to-driver-in-batch.md) | PUT |  |
| [Create Task](actions/create-task.md) | POST |  |
| [Create Tasks in Batch](actions/create-tasks-in-batch.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task](actions/get-task.md) | GET |  |
| [Search Tasks](actions/search-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |
| [Update Task Status in Batch](actions/update-task-status-in-batch.md) | PUT |  |
| [Update Tasks in Batch](actions/update-tasks-in-batch.md) | PUT |  |

### Taskfile

| Action | Method | Description |
| --- | --- | --- |
| [List Task POD/POC Files](actions/list-task-podpoc-files.md) | GET |  |

### Taskpackage

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Packages in Batch](actions/create-task-packages-in-batch.md) | POST |  |
| [Delete Task Package](actions/delete-task-package.md) | DELETE |  |
| [Get Task Package](actions/get-task-package.md) | GET |  |
| [Search Task Packages](actions/search-task-packages.md) | GET |  |
| [Update Task Package](actions/update-task-package.md) | PUT |  |

