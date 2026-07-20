# <img src="https://images.mindcloud.co/apps/icons/q-stash_1776783252436.png" alt="QStash logo" width="28" height="28"> QStash: Universal API

QStash is Upstash's HTTP-based message queue and scheduler for reliably publishing, enqueueing, scheduling, and inspecting webhook deliveries.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qStash/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://upstash.com/qstash
- **Vendor API docs:** https://upstash.com/docs/qstash/overall/getstarted

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Schedules](actions/list-schedules.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get URL Group](actions/get-url-group.md) | GET | Retrieves a URL Group from QStash by name. |
| [List URL Groups](actions/list-url-groups.md) | GET | Retrieves all URL Groups from QStash. |
| [Remove URL Group](actions/remove-url-group.md) | DELETE | Deletes a URL Group from QStash. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Cancel Messages](actions/bulk-cancel-messages.md) | DELETE | Cancels multiple messages in QStash by ID. |
| [Cancel Message](actions/cancel-message.md) | DELETE | Cancels a queued or scheduled message in QStash. |
| [Enqueue Message](actions/enqueue-message.md) | POST | Enqueues a message in a QStash queue. |
| [Get DLQ Message](actions/get-dlq-message.md) | GET | Retrieves a dead-letter queue message from QStash. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from QStash by ID. |
| [List DLQ Messages](actions/list-dlq-messages.md) | GET | Retrieves all dead-letter queue messages from QStash. |
| [Publish Message](actions/publish-message.md) | POST | Publishes a message to a QStash destination. |

### Queues

| Action | Method | Description |
| --- | --- | --- |
| [Delete Queue](actions/delete-queue.md) | DELETE | Deletes an existing queue from QStash. |
| [Get Queue](actions/get-queue.md) | GET | Retrieves a queue from QStash by name. |
| [Pause Queue](actions/pause-queue.md) | PUT | Pauses an existing queue in QStash. |
| [Resume Queue](actions/resume-queue.md) | PUT | Resumes a paused queue in QStash. |
| [Upsert Queue](actions/upsert-queue.md) | POST | Creates a QStash queue, or updates one if it exists. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a recurring delivery schedule in QStash. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes an existing schedule from QStash. |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves a schedule from QStash by ID. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves all existing schedules from QStash. |
| [Pause Schedule](actions/pause-schedule.md) | PUT | Pauses an existing schedule in QStash. |
| [Resume Schedule](actions/resume-schedule.md) | PUT | Resumes a paused schedule in QStash. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Get Signing Keys](actions/get-signing-keys.md) | GET | Retrieves the current signing keys from QStash. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Add URL Group Endpoints](actions/add-url-group-endpoints.md) | POST | Adds endpoints to a QStash URL Group, creating it if needed. |
| [Remove URL Group Endpoints](actions/remove-url-group-endpoints.md) | DELETE | Removes endpoints from a QStash URL Group. |

