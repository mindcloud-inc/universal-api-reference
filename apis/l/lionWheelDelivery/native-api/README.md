# LionWheel Delivery: Native API Reference

A consolidated summary of LionWheel Delivery's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://github.com/lionwheel/api
- **API base URL:** `https://test.lionwheel.com/api/v1`

## Authentication

### API Key

Use a LionWheel API key passed as the documented `key` query parameter on each REST request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/lionwheel/api#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | `POST /tasks/create` | [docs](https://github.com/lionwheel/api#create-a-delivery) |
| [Find Tasks by Order ID](actions/find-tasks-by-order-id.md) | `GET /tasks/by_order_id/:order_id` | [docs](https://github.com/lionwheel/api#get-tasks-by-order-id) |
| [Find Tasks by Phone](actions/find-tasks-by-phone.md) | `GET /tasks/by_phone/:phone` | [docs](https://github.com/lionwheel/api#get-tasks-by-phone) |
| [Get Task](actions/get-task.md) | `GET /tasks/show/:task_id` | [docs](https://github.com/lionwheel/api#receiving-delivery) |
| [Get Visit](actions/get-visit.md) | `GET /visits/:visit_id` | [docs](https://github.com/lionwheel/api#receiving-visit) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:task_id/update` | [docs](https://github.com/lionwheel/api#update-task) |
| [Update Visit](actions/update-visit.md) | `PUT /visits/:visit_id` | [docs](https://github.com/lionwheel/api#update-visit) |
