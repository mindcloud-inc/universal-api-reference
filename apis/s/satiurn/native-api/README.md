# Satiurn: Native API Reference

A consolidated summary of Satiurn's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.satiurn.com/
- **API base URL:** `https://publicapi.satiurn.com`

## Authentication

### API Key

Authenticate Satiurn API requests with the API secret key and business ID headers.

### Credentials

- **API Key:** `apiKey` · required
- **Business ID:** `businessId` · required · Satiurn BUSINESS_ID from Settings > API. Sent as the required `business` header by the REST API configuration.

Send these headers with each API request:

```http
apikey: <apiKey>
business: <businessId>
```

[Official authentication documentation](https://docs.satiurn.com/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | `POST /board/board` | [docs](https://docs.satiurn.com/t/boards/post/board/board) |
| [Create Category](actions/create-category.md) | `POST /finance/category` | [docs](https://docs.satiurn.com/t/categories/post/finance/category) |
| [Create Issue](actions/create-issue.md) | `POST /board/issue` | [docs](https://docs.satiurn.com/t/issues/post/board/issue) |
| [Create Label](actions/create-label.md) | `POST /label/label` | [docs](https://docs.satiurn.com/t/labels/post/label/label) |
| [Create Movement](actions/create-movement.md) | `POST /finance/movement` | [docs](https://docs.satiurn.com/t/movements/post/finance/movement) |
| [Create Pipeline](actions/create-pipeline.md) | `POST /board/pipeline` | [docs](https://docs.satiurn.com/t/pipelines/post/board/pipeline) |
| [Create Proposal](actions/create-proposal.md) | `POST /proposal/proposal` | [docs](https://docs.satiurn.com/t/proposals/post/proposal/proposal) |
| [Create Reminder](actions/create-reminder.md) | `POST /calendar/reminder` | [docs](https://docs.satiurn.com/t/reminders/post/calendar/reminder) |
| [Create Resource](actions/create-resource.md) | `POST /resource/resource` | [docs](https://docs.satiurn.com/t/resources/post/resource/resource) |
| [Create Stadium](actions/create-stadium.md) | `POST /proposal/stadium` | [docs](https://docs.satiurn.com/t/stadiums/post/proposal/stadium) |
| [Create Task](actions/create-task.md) | `POST /board/task` | [docs](https://docs.satiurn.com/t/tasks/post/board/task) |
| [Get Board](actions/get-board.md) | `GET /board/board` | [docs](https://docs.satiurn.com/t/boards/get/board/board) |
| [Get Boards](actions/get-boards.md) | `GET /board/boards` | [docs](https://docs.satiurn.com/t/boards/get/board/boards) |
| [Get Calendar Entities](actions/get-calendar-entities.md) | `GET /common/calendar` | [docs](https://docs.satiurn.com/t/calendar/get/common/calendar) |
| [Get Categories](actions/get-categories.md) | `GET /finance/category` | [docs](https://docs.satiurn.com/t/categories/get/finance/category) |
| [Get Issue](actions/get-issue.md) | `GET /board/issue` | [docs](https://docs.satiurn.com/t/issues/get/board/issue) |
| [Get Issues](actions/get-issues.md) | `GET /board/issues` | [docs](https://docs.satiurn.com/t/issues/get/board/issues) |
| [Get Labels](actions/get-labels.md) | `GET /label/labels` | [docs](https://docs.satiurn.com/t/labels/get/label/labels) |
| [Get Movement](actions/get-movement.md) | `GET /finance/movement` | [docs](https://docs.satiurn.com/t/movements/get/finance/movement) |
| [Get Pipelines](actions/get-pipelines.md) | `GET /board/pipelines` | [docs](https://docs.satiurn.com/t/pipelines/get/board/pipelines) |
| [Get Proposal](actions/get-proposal.md) | `GET /proposal/proposal` | [docs](https://docs.satiurn.com/t/proposals/get/proposal/proposal) |
| [Get Proposals](actions/get-proposals.md) | `GET /proposal/proposals` | [docs](https://docs.satiurn.com/t/proposals/get/proposal/proposals) |
| [Get Reminder](actions/get-reminder.md) | `GET /calendar/reminder` | [docs](https://docs.satiurn.com/t/reminders/get/calendar/reminder) |
| [Get Resource](actions/get-resource.md) | `GET /resource/resource` | [docs](https://docs.satiurn.com/t/resources/get/resource/resource) |
| [Get Resources](actions/get-resources.md) | `GET /resource/resources` | [docs](https://docs.satiurn.com/t/resources/get/resource/resources) |
| [Get Stadiums](actions/get-stadiums.md) | `GET /proposal/stadium` | [docs](https://docs.satiurn.com/t/stadiums/get/proposal/stadium) |
| [Get Subtask](actions/get-subtask.md) | `GET /board/subtask` | [docs](https://docs.satiurn.com/t/tasks/get/board/subtask) |
| [Get Subtasks](actions/get-subtasks.md) | `GET /board/subtasks` | [docs](https://docs.satiurn.com/t/tasks/get/board/subtasks) |
| [Get Task](actions/get-task.md) | `GET /board/task` | [docs](https://docs.satiurn.com/t/tasks/get/board/task) |
| [Update Board](actions/update-board.md) | `PUT /board/board` | [docs](https://docs.satiurn.com/t/boards/put/board/board) |
| [Update Category](actions/update-category.md) | `PUT /finance/category` | [docs](https://docs.satiurn.com/t/categories/put/finance/category) |
| [Update Issue](actions/update-issue.md) | `PUT /board/issue` | [docs](https://docs.satiurn.com/t/issues/put/board/issue) |
| [Update Label](actions/update-label.md) | `PUT /label/label` | [docs](https://docs.satiurn.com/t/labels/put/label/label) |
| [Update Movement](actions/update-movement.md) | `PUT /finance/movement` | [docs](https://docs.satiurn.com/t/movements/put/finance/movement) |
| [Update Pipeline](actions/update-pipeline.md) | `PUT /board/pipeline` | [docs](https://docs.satiurn.com/t/pipelines/put/board/pipeline) |
| [Update Proposal](actions/update-proposal.md) | `PUT /proposal/proposal` | [docs](https://docs.satiurn.com/t/proposals/put/proposal/proposal) |
| [Update Reminder](actions/update-reminder.md) | `PUT /calendar/reminder` | [docs](https://docs.satiurn.com/t/reminders/put/calendar/reminder) |
| [Update Resource](actions/update-resource.md) | `PUT /resource/resource` | [docs](https://docs.satiurn.com/t/resources/put/resource/resource) |
| [Update Stadium](actions/update-stadium.md) | `PUT /proposal/stadium` | [docs](https://docs.satiurn.com/t/stadiums/put/proposal/stadium) |
| [Update Task](actions/update-task.md) | `PUT /board/task` | [docs](https://docs.satiurn.com/t/tasks/put/board/task) |
