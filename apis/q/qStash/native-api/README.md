# QStash: Native API Reference

A consolidated summary of QStash's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://upstash.com/docs/qstash/overall/getstarted
- **API base URL:** `https://qstash-eu-central-1.upstash.io`

## Authentication

### QStash Token

Authenticate requests with a QStash token in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://upstash.com/docs/qstash/api/authentication)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add URL Group Endpoints](actions/add-url-group-endpoints.md) | `POST /v2/topics/:urlGroupName/endpoints` | [docs](https://upstash.com/docs/qstash/howto/url-group-endpoint) |
| [Bulk Cancel Messages](actions/bulk-cancel-messages.md) | `DELETE /v2/messages` | [docs](https://upstash.com/docs/qstash/api-refence/messages/bulk-cancel-messages) |
| [Cancel Message](actions/cancel-message.md) | `DELETE /v2/messages/:messageId` | [docs](https://upstash.com/docs/qstash/api-refence/messages/cancel-a-message) |
| [Create Schedule](actions/create-schedule.md) | `POST /v2/schedules/:destination` | [docs](https://upstash.com/docs/qstash/api-refence/schedules/create-a-schedule) |
| [Delete Queue](actions/delete-queue.md) | `DELETE /v2/queues/:queueName` | [docs](https://upstash.com/docs/qstash/api-refence/queues/delete-a-queue) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /v2/schedules/:scheduleId` | [docs](https://upstash.com/docs/qstash/api-refence/schedules/delete-a-schedule) |
| [Enqueue Message](actions/enqueue-message.md) | `POST /v2/enqueue/:queueName/:destination` | [docs](https://upstash.com/docs/qstash/api-refence/messages/enqueue-a-message) |
| [Get DLQ Message](actions/get-dlq-message.md) | `GET /v2/dlq/:dlqId` | [docs](https://upstash.com/docs/qstash/api-refence/dlq/get-a-dlq-message) |
| [Get Message](actions/get-message.md) | `GET /v2/messages/:messageId` | [docs](https://upstash.com/docs/qstash/api-refence/messages/get-a-message) |
| [Get Queue](actions/get-queue.md) | `GET /v2/queues/:queueName` | [docs](https://upstash.com/docs/qstash/api-refence/queues/get-a-queue) |
| [Get Schedule](actions/get-schedule.md) | `GET /v2/schedules/:scheduleId` | [docs](https://upstash.com/docs/qstash/api-refence/schedules/get-a-schedule) |
| [Get Signing Keys](actions/get-signing-keys.md) | `GET /v2/keys` | [docs](https://upstash.com/docs/qstash/api-refence/signing-keys/get-signing-keys) |
| [Get URL Group](actions/get-url-group.md) | `GET /v2/topics/:urlGroupName` | [docs](https://upstash.com/docs/qstash/api-refence/url-groups/get-a-url-group) |
| [List DLQ Messages](actions/list-dlq-messages.md) | `GET /v2/dlq` | [docs](https://upstash.com/docs/qstash/api-refence/dlq/list-dlq-messages) |
| [List Schedules](actions/list-schedules.md) | `GET /v2/schedules` | [docs](https://upstash.com/docs/qstash/api-refence/schedules/list-schedules) |
| [List URL Groups](actions/list-url-groups.md) | `GET /v2/topics` | [docs](https://upstash.com/docs/qstash/sdks/ts/examples/url-groups) |
| [Pause Queue](actions/pause-queue.md) | `POST /v2/queues/:queueName/pause` | [docs](https://upstash.com/docs/qstash/api-refence/queues/pause-queue) |
| [Pause Schedule](actions/pause-schedule.md) | `POST /v2/schedules/:scheduleId/pause` | [docs](https://upstash.com/docs/qstash/api-refence/schedules/pause-a-schedule) |
| [Publish Message](actions/publish-message.md) | `POST /v2/publish/:destination` | [docs](https://upstash.com/docs/qstash/api-refence/messages/publish-a-message) |
| [Remove URL Group](actions/remove-url-group.md) | `DELETE /v2/topics/:urlGroupName` | [docs](https://upstash.com/docs/qstash/api/url-groups/remove) |
| [Remove URL Group Endpoints](actions/remove-url-group-endpoints.md) | `DELETE /v2/topics/:urlGroupName/endpoints` | [docs](https://upstash.com/docs/qstash/sdks/ts/examples/url-groups) |
| [Resume Queue](actions/resume-queue.md) | `POST /v2/queues/:queueName/resume` | [docs](https://upstash.com/docs/qstash/api-refence/queues/resume-queue) |
| [Resume Schedule](actions/resume-schedule.md) | `POST /v2/schedules/:scheduleId/resume` | [docs](https://upstash.com/docs/qstash/api-refence/schedules/resume-a-schedule) |
| [Upsert Queue](actions/upsert-queue.md) | `POST /v2/queues` | [docs](https://upstash.com/docs/qstash/api-refence/queues/upsert-a-queue) |
