# Svix: Native API Reference

A consolidated summary of Svix's API configuration and 128 documented operations, with links to official documentation.

- **Official docs:** https://api.svix.com/docs
- **OpenAPI specification:** https://api.svix.com/api/v1/openapi.json
- **API base URL:** `https://api.us.svix.com`

## Authentication

### API Key

Authenticate Svix requests with the workspace API key sent as an HTTP bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.svix.com/docs)

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–250).

## Sorting

Set the sort field with `order` in the query string. Use `ascending` for ascending order and `descending` for descending order. Only one sort field is accepted.

## Endpoints (128 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Aggregate App Stats](actions/aggregate-app-stats.md) | `POST /api/v1/stats/usage/app` | [docs](https://api.svix.com/docs#operation/v1.statistics.aggregate-app-stats) |
| [Aggregate Event Types](actions/aggregate-event-types.md) | `PUT /api/v1/stats/usage/event-types` | [docs](https://api.svix.com/docs#operation/v1.statistics.aggregate-event-types) |
| [Bulk Replay Messages](actions/bulk-replay-messages.md) | `POST /api/v1/app/{app_id}/endpoint/{endpoint_id}/bulk-replay` | [docs](https://api.svix.com/docs#operation/v1.endpoint.bulk-replay) |
| [Create Application](actions/create-application.md) | `POST /api/v1/app` | [docs](https://api.svix.com/docs#operation/v1.application.create) |
| [Create Connector](actions/create-connector.md) | `POST /api/v1/connector` | [docs](https://api.svix.com/docs#operation/v1.connector.create) |
| [Create Endpoint](actions/create-endpoint.md) | `POST /api/v1/app/{app_id}/endpoint` | [docs](https://api.svix.com/docs#operation/v1.endpoint.create) |
| [Create Event Type](actions/create-event-type.md) | `POST /api/v1/event-type` | [docs](https://api.svix.com/docs#operation/v1.event-type.create) |
| [Create Events](actions/create-events.md) | `POST /api/v1/stream/{stream_id}/events` | [docs](https://api.svix.com/docs#operation/v1.streaming.events.create) |
| [Create Ingest Endpoint](actions/create-ingest-endpoint.md) | `POST /ingest/api/v1/source/{source_id}/endpoint` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.create) |
| [Create Ingest Source](actions/create-ingest-source.md) | `POST /ingest/api/v1/source` | [docs](https://api.svix.com/docs#operation/v1.ingest.source.create) |
| [Create Integration](actions/create-integration.md) | `POST /api/v1/app/{app_id}/integration` | [docs](https://api.svix.com/docs#operation/v1.integration.create) |
| [Create Message](actions/create-message.md) | `POST /api/v1/app/{app_id}/msg` | [docs](https://api.svix.com/docs#operation/v1.message.create) |
| [Create Message Precheck](actions/create-message-precheck.md) | `POST /api/v1/app/{app_id}/msg/precheck/active` | [docs](https://api.svix.com/docs#operation/v1.message.precheck) |
| [Create Operational Webhook Endpoint](actions/create-operational-webhook-endpoint.md) | `POST /api/v1/operational-webhook/endpoint` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.create) |
| [Create Sink](actions/create-sink.md) | `POST /api/v1/stream/{stream_id}/sink` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.create) |
| [Create Stream](actions/create-stream.md) | `POST /api/v1/stream` | [docs](https://api.svix.com/docs#operation/v1.streaming.stream.create) |
| [Create Stream Event Type](actions/create-stream-event-type.md) | `POST /api/v1/stream/event-type` | [docs](https://api.svix.com/docs#operation/v1.streaming.event-type.create) |
| [Delete Application](actions/delete-application.md) | `DELETE /api/v1/app/{app_id}` | [docs](https://api.svix.com/docs#operation/v1.application.delete) |
| [Delete Attempt Response Body](actions/delete-attempt-response-body.md) | `DELETE /api/v1/app/{app_id}/msg/{msg_id}/attempt/{attempt_id}/content` | [docs](https://api.svix.com/docs#operation/v1.message-attempt.expunge-content) |
| [Delete Connector](actions/delete-connector.md) | `DELETE /api/v1/connector/{connector_id}` | [docs](https://api.svix.com/docs#operation/v1.connector.delete) |
| [Delete Endpoint](actions/delete-endpoint.md) | `DELETE /api/v1/app/{app_id}/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.endpoint.delete) |
| [Delete Event Type](actions/delete-event-type.md) | `DELETE /api/v1/event-type/{event_type_name}` | [docs](https://api.svix.com/docs#operation/v1.event-type.delete) |
| [Delete Ingest Endpoint](actions/delete-ingest-endpoint.md) | `DELETE /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.delete) |
| [Delete Ingest Source](actions/delete-ingest-source.md) | `DELETE /ingest/api/v1/source/{source_id}` | [docs](https://api.svix.com/docs#operation/v1.ingest.source.delete) |
| [Delete Integration](actions/delete-integration.md) | `DELETE /api/v1/app/{app_id}/integration/{integ_id}` | [docs](https://api.svix.com/docs#operation/v1.integration.delete) |
| [Delete Message Payload](actions/delete-message-payload.md) | `DELETE /api/v1/app/{app_id}/msg/{msg_id}/content` | [docs](https://api.svix.com/docs#operation/v1.message.expunge-content) |
| [Delete Operational Webhook Endpoint](actions/delete-operational-webhook-endpoint.md) | `DELETE /api/v1/operational-webhook/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.delete) |
| [Delete Sink](actions/delete-sink.md) | `DELETE /api/v1/stream/{stream_id}/sink/{sink_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.delete) |
| [Delete Stream](actions/delete-stream.md) | `DELETE /api/v1/stream/{stream_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.stream.delete) |
| [Delete Stream Event Type](actions/delete-stream-event-type.md) | `DELETE /api/v1/stream/event-type/{name}` | [docs](https://api.svix.com/docs#operation/v1.streaming.event-type.delete) |
| [Endpoint Stats](actions/endpoint-stats.md) | `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}/stats` | [docs](https://api.svix.com/docs#operation/v1.endpoint.get-stats) |
| [Event Type Import From Openapi](actions/event-type-import-from-openapi.md) | `POST /api/v1/event-type/import/openapi` | [docs](https://api.svix.com/docs#operation/v1.event-type.import-openapi) |
| [Expire All](actions/expire-all.md) | `POST /api/v1/auth/app/{app_id}/expire-all` | [docs](https://api.svix.com/docs#operation/v1.authentication.expire-all) |
| [Export Environment Configuration](actions/export-environment-configuration.md) | `POST /api/v1/environment/export` | [docs](https://api.svix.com/docs#operation/v1.environment.export) |
| [Expunge All Message Contents](actions/expunge-all-message-contents.md) | `POST /api/v1/app/{app_id}/msg/expunge-all-contents` | [docs](https://api.svix.com/docs#operation/v1.message.expunge-all-contents) |
| [Get Application](actions/get-application.md) | `GET /api/v1/app/{app_id}` | [docs](https://api.svix.com/docs#operation/v1.application.get) |
| [Get Attempt](actions/get-attempt.md) | `GET /api/v1/app/{app_id}/msg/{msg_id}/attempt/{attempt_id}` | [docs](https://api.svix.com/docs#operation/v1.message-attempt.get) |
| [Get Background Task](actions/get-background-task.md) | `GET /api/v1/background-task/{task_id}` | [docs](https://api.svix.com/docs#operation/v1.background-task.get) |
| [Get Connector](actions/get-connector.md) | `GET /api/v1/connector/{connector_id}` | [docs](https://api.svix.com/docs#operation/v1.connector.get) |
| [Get Consumer App Portal Access](actions/get-consumer-app-portal-access.md) | `POST /api/v1/auth/app-portal-access/{app_id}` | [docs](https://api.svix.com/docs#operation/v1.authentication.app-portal-access) |
| [Get Endpoint](actions/get-endpoint.md) | `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.endpoint.get) |
| [Get Endpoint Headers](actions/get-endpoint-headers.md) | `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.endpoint.get-headers) |
| [Get Endpoint Secret](actions/get-endpoint-secret.md) | `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}/secret` | [docs](https://api.svix.com/docs#operation/v1.endpoint.get-secret) |
| [Get Endpoint Transformation](actions/get-endpoint-transformation.md) | `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}/transformation` | [docs](https://api.svix.com/docs#operation/v1.endpoint.transformation-get) |
| [Get Event Type](actions/get-event-type.md) | `GET /api/v1/event-type/{event_type_name}` | [docs](https://api.svix.com/docs#operation/v1.event-type.get) |
| [Get Ingest Endpoint](actions/get-ingest-endpoint.md) | `GET /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.get) |
| [Get Ingest Endpoint Headers](actions/get-ingest-endpoint-headers.md) | `GET /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.get-headers) |
| [Get Ingest Endpoint Secret](actions/get-ingest-endpoint-secret.md) | `GET /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}/secret` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.get-secret) |
| [Get Ingest Endpoint Transformation](actions/get-ingest-endpoint-transformation.md) | `GET /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}/transformation` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.get-transformation) |
| [Get Ingest Source](actions/get-ingest-source.md) | `GET /ingest/api/v1/source/{source_id}` | [docs](https://api.svix.com/docs#operation/v1.ingest.source.get) |
| [Get Integration](actions/get-integration.md) | `GET /api/v1/app/{app_id}/integration/{integ_id}` | [docs](https://api.svix.com/docs#operation/v1.integration.get) |
| [Get Integration Key](actions/get-integration-key.md) | `GET /api/v1/app/{app_id}/integration/{integ_id}/key` | [docs](https://api.svix.com/docs#operation/v1.integration.get-key) |
| [Get Message](actions/get-message.md) | `GET /api/v1/app/{app_id}/msg/{msg_id}` | [docs](https://api.svix.com/docs#operation/v1.message.get) |
| [Get Operational Webhook Endpoint](actions/get-operational-webhook-endpoint.md) | `GET /api/v1/operational-webhook/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.get) |
| [Get Operational Webhook Endpoint Headers](actions/get-operational-webhook-endpoint-headers.md) | `GET /api/v1/operational-webhook/endpoint/{endpoint_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.get-headers) |
| [Get Operational Webhook Endpoint Secret](actions/get-operational-webhook-endpoint-secret.md) | `GET /api/v1/operational-webhook/endpoint/{endpoint_id}/secret` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.get-secret) |
| [Get Poller Token](actions/get-poller-token.md) | `GET /api/v1/auth/stream/{stream_id}/sink/{sink_id}/poller/token` | [docs](https://api.svix.com/docs#operation/v1.authentication.get-stream-poller-token) |
| [Get Sink](actions/get-sink.md) | `GET /api/v1/stream/{stream_id}/sink/{sink_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.get) |
| [Get Sink Headers](actions/get-sink-headers.md) | `GET /api/v1/stream/{stream_id}/sink/{sink_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink-headers-get) |
| [Get Sink Secret](actions/get-sink-secret.md) | `GET /api/v1/stream/{stream_id}/sink/{sink_id}/secret` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.get-secret) |
| [Get Sink Transformation](actions/get-sink-transformation.md) | `GET /api/v1/stream/{stream_id}/sink/{sink_id}/transformation` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink-transformation-get) |
| [Get Stream](actions/get-stream.md) | `GET /api/v1/stream/{stream_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.stream.get) |
| [Get Stream Event Type](actions/get-stream-event-type.md) | `GET /api/v1/stream/event-type/{name}` | [docs](https://api.svix.com/docs#operation/v1.streaming.event-type.get) |
| [Get Stream Portal Access](actions/get-stream-portal-access.md) | `POST /api/v1/auth/stream-portal-access/{stream_id}` | [docs](https://api.svix.com/docs#operation/v1.authentication.stream-portal-access) |
| [Health](actions/health.md) | `GET /api/v1/health` | [docs](https://api.svix.com/docs#operation/v1.health.get) |
| [Import Environment Configuration](actions/import-environment-configuration.md) | `POST /api/v1/environment/import` | [docs](https://api.svix.com/docs#operation/v1.environment.import) |
| [Ingest Source Consumer Portal](actions/ingest-source-consumer-portal.md) | `POST /ingest/api/v1/source/{source_id}/dashboard` | [docs](https://api.svix.com/docs#operation/v1.ingest.dashboard) |
| [List Applications](actions/list-applications.md) | `GET /api/v1/app` | [docs](https://api.svix.com/docs#operation/v1.application.list) |
| [List Attempted Destinations](actions/list-attempted-destinations.md) | `GET /api/v1/app/{app_id}/msg/{msg_id}/endpoint` | [docs](https://api.svix.com/docs#operation/v1.message-attempt.list-attempted-destinations) |
| [List Attempted Messages](actions/list-attempted-messages.md) | `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}/msg` | [docs](https://api.svix.com/docs#operation/v1.message-attempt.list-attempted-messages) |
| [List Attempts By Endpoint](actions/list-attempts-by-endpoint.md) | `GET /api/v1/app/{app_id}/attempt/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.message-attempt.list-by-endpoint) |
| [List Attempts By Msg](actions/list-attempts-by-msg.md) | `GET /api/v1/app/{app_id}/attempt/msg/{msg_id}` | [docs](https://api.svix.com/docs#operation/v1.message-attempt.list-by-msg) |
| [List Background Tasks](actions/list-background-tasks.md) | `GET /api/v1/background-task` | [docs](https://api.svix.com/docs#operation/v1.background-task.list) |
| [List Connectors](actions/list-connectors.md) | `GET /api/v1/connector` | [docs](https://api.svix.com/docs#operation/v1.connector.list) |
| [List Endpoints](actions/list-endpoints.md) | `GET /api/v1/app/{app_id}/endpoint` | [docs](https://api.svix.com/docs#operation/v1.endpoint.list) |
| [List Event Types](actions/list-event-types.md) | `GET /api/v1/event-type` | [docs](https://api.svix.com/docs#operation/v1.event-type.list) |
| [List Ingest Endpoints](actions/list-ingest-endpoints.md) | `GET /ingest/api/v1/source/{source_id}/endpoint` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.list) |
| [List Ingest Sources](actions/list-ingest-sources.md) | `GET /ingest/api/v1/source` | [docs](https://api.svix.com/docs#operation/v1.ingest.source.list) |
| [List Integrations](actions/list-integrations.md) | `GET /api/v1/app/{app_id}/integration` | [docs](https://api.svix.com/docs#operation/v1.integration.list) |
| [List Messages](actions/list-messages.md) | `GET /api/v1/app/{app_id}/msg` | [docs](https://api.svix.com/docs#operation/v1.message.list) |
| [List Operational Webhook Endpoints](actions/list-operational-webhook-endpoints.md) | `GET /api/v1/operational-webhook/endpoint` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.list) |
| [List Sinks](actions/list-sinks.md) | `GET /api/v1/stream/{stream_id}/sink` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.list) |
| [List Stream Event Types](actions/list-stream-event-types.md) | `GET /api/v1/stream/event-type` | [docs](https://api.svix.com/docs#operation/v1.streaming.event-type.list) |
| [List Streams](actions/list-streams.md) | `GET /api/v1/stream` | [docs](https://api.svix.com/docs#operation/v1.streaming.stream.list) |
| [Logout](actions/logout.md) | `POST /api/v1/auth/logout` | [docs](https://api.svix.com/docs#operation/v1.authentication.logout) |
| [Patch Application](actions/patch-application.md) | `PATCH /api/v1/app/{app_id}` | [docs](https://api.svix.com/docs#operation/v1.application.patch) |
| [Patch Connector](actions/patch-connector.md) | `PATCH /api/v1/connector/{connector_id}` | [docs](https://api.svix.com/docs#operation/v1.connector.patch) |
| [Patch Endpoint](actions/patch-endpoint.md) | `PATCH /api/v1/app/{app_id}/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.endpoint.patch) |
| [Patch Endpoint Headers](actions/patch-endpoint-headers.md) | `PATCH /api/v1/app/{app_id}/endpoint/{endpoint_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.endpoint.patch-headers) |
| [Patch Endpoint Transformation](actions/patch-endpoint-transformation.md) | `PATCH /api/v1/app/{app_id}/endpoint/{endpoint_id}/transformation` | [docs](https://api.svix.com/docs#operation/v1.endpoint.patch-transformation) |
| [Patch Event Type](actions/patch-event-type.md) | `PATCH /api/v1/event-type/{event_type_name}` | [docs](https://api.svix.com/docs#operation/v1.event-type.patch) |
| [Patch Ingest Endpoint Transformation](actions/patch-ingest-endpoint-transformation.md) | `PATCH /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}/transformation` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.set-transformation) |
| [Patch Sink](actions/patch-sink.md) | `PATCH /api/v1/stream/{stream_id}/sink/{sink_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.patch) |
| [Patch Sink Headers](actions/patch-sink-headers.md) | `PATCH /api/v1/stream/{stream_id}/sink/{sink_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink-headers-patch) |
| [Patch Stream](actions/patch-stream.md) | `PATCH /api/v1/stream/{stream_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.stream.patch) |
| [Patch Stream Event Type](actions/patch-stream-event-type.md) | `PATCH /api/v1/stream/event-type/{name}` | [docs](https://api.svix.com/docs#operation/v1.streaming.event-type.patch) |
| [Poller Consumer Poll](actions/poller-consumer-poll.md) | `GET /api/v1/app/{app_id}/poller/{sink_id}/consumer/{consumer_id}` | [docs](https://api.svix.com/docs#operation/v1.message.poller.consumer-poll) |
| [Poller Consumer Seek](actions/poller-consumer-seek.md) | `POST /api/v1/app/{app_id}/poller/{sink_id}/consumer/{consumer_id}/seek` | [docs](https://api.svix.com/docs#operation/v1.message.poller.consumer-seek) |
| [Poller Poll](actions/poller-poll.md) | `GET /api/v1/app/{app_id}/poller/{sink_id}` | [docs](https://api.svix.com/docs#operation/v1.message.poller.poll) |
| [Poller Sink Stream Events](actions/poller-sink-stream-events.md) | `GET /api/v1/stream/{stream_id}/sink/{sink_id}/events` | [docs](https://api.svix.com/docs#operation/v1.streaming.events.get) |
| [Recover Failed Webhooks](actions/recover-failed-webhooks.md) | `POST /api/v1/app/{app_id}/endpoint/{endpoint_id}/recover` | [docs](https://api.svix.com/docs#operation/v1.endpoint.recover) |
| [Replay Missing Webhooks](actions/replay-missing-webhooks.md) | `POST /api/v1/app/{app_id}/endpoint/{endpoint_id}/replay-missing` | [docs](https://api.svix.com/docs#operation/v1.endpoint.replay-missing) |
| [Resend Webhook](actions/resend-webhook.md) | `POST /api/v1/app/{app_id}/msg/{msg_id}/endpoint/{endpoint_id}/resend` | [docs](https://api.svix.com/docs#operation/v1.message-attempt.resend) |
| [Rotate Endpoint Secret](actions/rotate-endpoint-secret.md) | `POST /api/v1/app/{app_id}/endpoint/{endpoint_id}/secret/rotate` | [docs](https://api.svix.com/docs#operation/v1.endpoint.rotate-secret) |
| [Rotate Ingest Endpoint Secret](actions/rotate-ingest-endpoint-secret.md) | `POST /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}/secret/rotate` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.rotate-secret) |
| [Rotate Ingest Token](actions/rotate-ingest-token.md) | `POST /ingest/api/v1/source/{source_id}/token/rotate` | [docs](https://api.svix.com/docs#operation/v1.ingest.source.rotate-token) |
| [Rotate Integration Key](actions/rotate-integration-key.md) | `POST /api/v1/app/{app_id}/integration/{integ_id}/key/rotate` | [docs](https://api.svix.com/docs#operation/v1.integration.rotate-key) |
| [Rotate Operational Webhook Endpoint Secret](actions/rotate-operational-webhook-endpoint-secret.md) | `POST /api/v1/operational-webhook/endpoint/{endpoint_id}/secret/rotate` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.rotate-secret) |
| [Rotate Poller Token](actions/rotate-poller-token.md) | `POST /api/v1/auth/stream/{stream_id}/sink/{sink_id}/poller/token/rotate` | [docs](https://api.svix.com/docs#operation/v1.authentication.rotate-stream-poller-token) |
| [Rotate Sink Secret](actions/rotate-sink-secret.md) | `POST /api/v1/stream/{stream_id}/sink/{sink_id}/secret/rotate` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.rotate-secret) |
| [Send Event Type Example Message](actions/send-event-type-example-message.md) | `POST /api/v1/app/{app_id}/endpoint/{endpoint_id}/send-example` | [docs](https://api.svix.com/docs#operation/v1.endpoint.send-example) |
| [Set Sink Transformation](actions/set-sink-transformation.md) | `PATCH /api/v1/stream/{stream_id}/sink/{sink_id}/transformation` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.transformation-partial-update) |
| [Stream Expire All](actions/stream-expire-all.md) | `POST /api/v1/auth/stream/{stream_id}/expire-all` | [docs](https://api.svix.com/docs#operation/v1.authentication.stream-expire-all) |
| [Stream Logout](actions/stream-logout.md) | `POST /api/v1/auth/stream-logout` | [docs](https://api.svix.com/docs#operation/v1.authentication.stream-logout) |
| [Update Application](actions/update-application.md) | `PUT /api/v1/app/{app_id}` | [docs](https://api.svix.com/docs#operation/v1.application.update) |
| [Update Connector](actions/update-connector.md) | `PUT /api/v1/connector/{connector_id}` | [docs](https://api.svix.com/docs#operation/v1.connector.update) |
| [Update Endpoint](actions/update-endpoint.md) | `PUT /api/v1/app/{app_id}/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.endpoint.update) |
| [Update Endpoint Headers](actions/update-endpoint-headers.md) | `PUT /api/v1/app/{app_id}/endpoint/{endpoint_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.endpoint.update-headers) |
| [Update Event Type](actions/update-event-type.md) | `PUT /api/v1/event-type/{event_type_name}` | [docs](https://api.svix.com/docs#operation/v1.event-type.update) |
| [Update Ingest Endpoint](actions/update-ingest-endpoint.md) | `PUT /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.update) |
| [Update Ingest Endpoint Headers](actions/update-ingest-endpoint-headers.md) | `PUT /ingest/api/v1/source/{source_id}/endpoint/{endpoint_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.ingest.endpoint.update-headers) |
| [Update Integration](actions/update-integration.md) | `PUT /api/v1/app/{app_id}/integration/{integ_id}` | [docs](https://api.svix.com/docs#operation/v1.integration.update) |
| [Update Operational Webhook Endpoint](actions/update-operational-webhook-endpoint.md) | `PUT /api/v1/operational-webhook/endpoint/{endpoint_id}` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.update) |
| [Update Operational Webhook Endpoint Headers](actions/update-operational-webhook-endpoint-headers.md) | `PUT /api/v1/operational-webhook/endpoint/{endpoint_id}/headers` | [docs](https://api.svix.com/docs#operation/v1.operational-webhook.endpoint.update-headers) |
| [Update Sink](actions/update-sink.md) | `PUT /api/v1/stream/{stream_id}/sink/{sink_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.sink.update) |
| [Update Source](actions/update-source.md) | `PUT /ingest/api/v1/source/{source_id}` | [docs](https://api.svix.com/docs#operation/v1.ingest.source.update) |
| [Update Stream](actions/update-stream.md) | `PUT /api/v1/stream/{stream_id}` | [docs](https://api.svix.com/docs#operation/v1.streaming.stream.update) |
| [Update Stream Event Type](actions/update-stream-event-type.md) | `PUT /api/v1/stream/event-type/{name}` | [docs](https://api.svix.com/docs#operation/v1.streaming.event-type.update) |
