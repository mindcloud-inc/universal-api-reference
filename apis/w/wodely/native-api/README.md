# Wodely: Native API Reference

A consolidated summary of Wodely's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://app.wodely.com/doc/api-documentation.html
- **API base URL:** `https://api.wodely.com`

## Authentication

### API Key

Connect with a Wodely organization API key. MindCloud sends the key in Wodely's required Authorization: Basic header format.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.wodely.com/integration/)

## API conventions

Response data is read from `data`. The next-page cursor is read from `lastId`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Tasks to Driver in Batch](actions/assign-tasks-to-driver-in-batch.md) | `POST /v2/tasks/driver` | [docs](https://app.wodely.com/doc/api-documentation.html#assign-task-to-driver) |
| [Create CloudWaitress Order](actions/create-cloudwaitress-order.md) | `POST /cloudwaitress/order` | [docs](https://www.wodely.com/project/cloudwaitress/) |
| [Create GloriaFood Job](actions/create-gloriafood-job.md) | `POST /gloriafood/job` | [docs](https://www.wodely.com/project/gloriafood/) |
| [Create Task](actions/create-task.md) | `POST /v2/tasks` | [docs](https://app.wodely.com/doc/api-documentation.html#create-task) |
| [Create Task Packages in Batch](actions/create-task-packages-in-batch.md) | `POST /v2/taskPackages` | [docs](https://app.wodely.com/doc/api-documentation.html#create-task-packages) |
| [Create Tasks in Batch](actions/create-tasks-in-batch.md) | `POST /v2/tasks/bulkcreate` | [docs](https://app.wodely.com/doc/api-documentation.html#create-task-batch) |
| [Create Yelo Order](actions/create-yelo-order.md) | `POST /yelo/order` | [docs](https://www.wodely.com/project/yelo/) |
| [Delete Task](actions/delete-task.md) | `DELETE /v2/tasks/[:taskGuid]` | [docs](https://app.wodely.com/doc/api-documentation.html#delete-task) |
| [Delete Task Package](actions/delete-task-package.md) | `DELETE /v2/taskPackages/[:packageId]` | [docs](https://app.wodely.com/doc/api-documentation.html#delete-task-package) |
| [Get Task](actions/get-task.md) | `POST /v2/tasks/get` | [docs](https://app.wodely.com/doc/api-documentation.html#get-single-task) |
| [Get Task Package](actions/get-task-package.md) | `GET /v2/taskPackages/[:packageId]` | [docs](https://app.wodely.com/doc/api-documentation.html#get-task-package) |
| [List Drivers](actions/list-drivers.md) | `GET /v2/drivers` | [docs](https://app.wodely.com/doc/api-documentation.html#get-drivers) |
| [List Task POD/POC Files](actions/list-task-podpoc-files.md) | `GET /v2/taskFiles/[:taskGuid]` | [docs](https://app.wodely.com/doc/api-documentation.html#get-task-files) |
| [Ping API](actions/ping-api.md) | `GET /ping` | [docs](https://app.wodely.com/doc/api-documentation.html#paraAuthentication) |
| [Search Routes](actions/search-routes.md) | `POST /v2/routes/search` | [docs](https://app.wodely.com/doc/api-documentation.html#get-routes) |
| [Search Task Packages](actions/search-task-packages.md) | `POST /v2/taskPackages/search` | [docs](https://app.wodely.com/doc/api-documentation.html#list-task-packages) |
| [Search Tasks](actions/search-tasks.md) | `POST /v2/tasks/search` | [docs](https://app.wodely.com/doc/api-documentation.html#list-tasks) |
| [Update Task](actions/update-task.md) | `PUT /v2/tasks/[:taskGuid]` | [docs](https://app.wodely.com/doc/api-documentation.html#update-task) |
| [Update Task Package](actions/update-task-package.md) | `PUT /v2/taskPackages/[:packageId]` | [docs](https://app.wodely.com/doc/api-documentation.html#update-task-package) |
| [Update Task Status in Batch](actions/update-task-status-in-batch.md) | `POST /v2/tasks/status` | [docs](https://app.wodely.com/doc/api-documentation.html#update-task-status) |
| [Update Tasks in Batch](actions/update-tasks-in-batch.md) | `POST /v2/tasks/bulkupdate` | [docs](https://app.wodely.com/doc/api-documentation.html#update-task-batch) |
