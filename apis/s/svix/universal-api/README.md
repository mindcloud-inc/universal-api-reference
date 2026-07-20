# <img src="https://images.mindcloud.co/apps/icons/svix-icon-square_1776352983054.png" alt="Svix logo" width="28" height="28"> Svix: Universal API

Svix is a webhook and event streaming platform for managing applications, endpoints, integrations, messages, streams, sinks, ingest sources, and operational webhooks through a single API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/svix/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 128
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.svix.com
- **Vendor API docs:** https://api.svix.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Applications](actions/list-applications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (128)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | POST | Creates an application in Svix. |
| [Delete Application](actions/delete-application.md) | DELETE | Deletes an application from Svix. |
| [Get Application](actions/get-application.md) | GET | Retrieves an application from Svix. |
| [List Applications](actions/list-applications.md) | GET | Retrieves applications from Svix. |
| [Patch Application](actions/patch-application.md) | PUT | Updates an application in Svix. |
| [Update Application](actions/update-application.md) | PUT | Updates an application in Svix. |

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Expire All](actions/expire-all.md) | POST | Expires all application tokens in Svix. |
| [Get Consumer App Portal Access](actions/get-consumer-app-portal-access.md) | POST | Retrieves consumer app portal access from Svix. |
| [Logout](actions/logout.md) | POST | Logs out an application token in Svix. |

### Background Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Background Task](actions/get-background-task.md) | GET | Retrieves a background task from Svix. |
| [List Background Tasks](actions/list-background-tasks.md) | GET | Retrieves background tasks from Svix. |

### Connector

| Action | Method | Description |
| --- | --- | --- |
| [Create Connector](actions/create-connector.md) | POST | Creates a connector in Svix. |
| [Delete Connector](actions/delete-connector.md) | DELETE | Deletes a connector from Svix. |
| [Get Connector](actions/get-connector.md) | GET | Retrieves a connector from Svix. |
| [List Connectors](actions/list-connectors.md) | GET | Retrieves connectors from Svix. |
| [Patch Connector](actions/patch-connector.md) | PUT | Updates a connector in Svix. |
| [Update Connector](actions/update-connector.md) | PUT | Updates a connector in Svix. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Replay Messages](actions/bulk-replay-messages.md) | POST | Replays messages for a specific Svix endpoint. |
| [Create Endpoint](actions/create-endpoint.md) | POST | Creates an endpoint in Svix. |
| [Delete Endpoint](actions/delete-endpoint.md) | DELETE | Deletes an endpoint from Svix. |
| [Endpoint Stats](actions/endpoint-stats.md) | GET | Retrieves statistics for a specific Svix endpoint. |
| [Get Endpoint](actions/get-endpoint.md) | GET | Retrieves an endpoint from Svix. |
| [Get Endpoint Headers](actions/get-endpoint-headers.md) | GET | Retrieves endpoint headers from Svix. |
| [Get Endpoint Secret](actions/get-endpoint-secret.md) | GET | Retrieves an endpoint secret from Svix. |
| [Get Endpoint Transformation](actions/get-endpoint-transformation.md) | GET | Retrieves an endpoint transformation from Svix. |
| [List Endpoints](actions/list-endpoints.md) | GET | Retrieves endpoints from Svix. |
| [Patch Endpoint](actions/patch-endpoint.md) | PUT | Updates an endpoint in Svix. |
| [Patch Endpoint Headers](actions/patch-endpoint-headers.md) | PUT | Updates endpoint headers in Svix. |
| [Patch Endpoint Transformation](actions/patch-endpoint-transformation.md) | PUT | Updates an endpoint transformation in Svix. |
| [Recover Failed Webhooks](actions/recover-failed-webhooks.md) | POST | Recovers failed webhooks for a specific Svix endpoint. |
| [Replay Missing Webhooks](actions/replay-missing-webhooks.md) | POST | Replays missing webhooks to a specific Svix endpoint. |
| [Rotate Endpoint Secret](actions/rotate-endpoint-secret.md) | POST | Rotates an endpoint secret in Svix. |
| [Send Event Type Example Message](actions/send-event-type-example-message.md) | POST | Sends an example event message to a Svix endpoint. |
| [Update Endpoint](actions/update-endpoint.md) | PUT | Updates an endpoint in Svix. |
| [Update Endpoint Headers](actions/update-endpoint-headers.md) | PUT | Updates endpoint headers in Svix. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Export Environment Configuration](actions/export-environment-configuration.md) | POST | Exports environment configuration from Svix. |
| [Import Environment Configuration](actions/import-environment-configuration.md) | POST | Imports environment configuration into Svix. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Events](actions/create-events.md) | POST | Creates stream events in Svix. |
| [Poller Sink Stream Events](actions/poller-sink-stream-events.md) | GET | Retrieves stream events from a Svix sink. |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Type](actions/create-event-type.md) | POST | Creates or unarchives an event type in Svix. |
| [Delete Event Type](actions/delete-event-type.md) | DELETE | Archives an event type in Svix. |
| [Event Type Import From Openapi](actions/event-type-import-from-openapi.md) | POST | Imports event types from an OpenAPI spec into Svix. |
| [Get Event Type](actions/get-event-type.md) | GET | Retrieves an event type from Svix. |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves event types from Svix. |
| [Patch Event Type](actions/patch-event-type.md) | PUT | Updates an event type in Svix. |
| [Update Event Type](actions/update-event-type.md) | PUT | Updates an event type in Svix. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Health](actions/health.md) | GET | Verifies the Svix API is running. |

### Ingest Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Ingest Endpoint](actions/create-ingest-endpoint.md) | POST | Creates an ingest endpoint in Svix. |
| [Delete Ingest Endpoint](actions/delete-ingest-endpoint.md) | DELETE | Deletes an ingest endpoint from Svix. |
| [Get Ingest Endpoint](actions/get-ingest-endpoint.md) | GET | Retrieves an ingest endpoint from Svix. |
| [Get Ingest Endpoint Headers](actions/get-ingest-endpoint-headers.md) | GET | Retrieves ingest endpoint headers from Svix. |
| [Get Ingest Endpoint Secret](actions/get-ingest-endpoint-secret.md) | GET | Retrieves an ingest endpoint secret from Svix. |
| [Get Ingest Endpoint Transformation](actions/get-ingest-endpoint-transformation.md) | GET | Retrieves an ingest endpoint transformation from Svix. |
| [List Ingest Endpoints](actions/list-ingest-endpoints.md) | GET | Retrieves ingest endpoints from Svix. |
| [Patch Ingest Endpoint Transformation](actions/patch-ingest-endpoint-transformation.md) | PUT | Updates an ingest endpoint transformation in Svix. |
| [Rotate Ingest Endpoint Secret](actions/rotate-ingest-endpoint-secret.md) | POST | Rotates an ingest endpoint secret in Svix. |
| [Update Ingest Endpoint](actions/update-ingest-endpoint.md) | PUT | Updates an ingest endpoint in Svix. |
| [Update Ingest Endpoint Headers](actions/update-ingest-endpoint-headers.md) | PUT | Updates ingest endpoint headers in Svix. |

### Ingest Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Ingest Source](actions/create-ingest-source.md) | POST | Creates an ingest source in Svix. |
| [Delete Ingest Source](actions/delete-ingest-source.md) | DELETE | Deletes an ingest source from Svix. |
| [Get Ingest Source](actions/get-ingest-source.md) | GET | Retrieves an ingest source from Svix. |
| [Ingest Source Consumer Portal](actions/ingest-source-consumer-portal.md) | POST | Retrieves ingest source portal access from Svix. |
| [List Ingest Sources](actions/list-ingest-sources.md) | GET | Retrieves ingest sources from Svix. |
| [Rotate Ingest Token](actions/rotate-ingest-token.md) | POST | Rotates an ingest source token in Svix. |
| [Update Source](actions/update-source.md) | PUT | Updates an ingest source in Svix. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration](actions/create-integration.md) | POST | Creates an integration in Svix. |
| [Delete Integration](actions/delete-integration.md) | DELETE | Deletes an integration from Svix. |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from Svix. |
| [Get Integration Key](actions/get-integration-key.md) | GET | Retrieves an integration key from Svix. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from Svix. |
| [Rotate Integration Key](actions/rotate-integration-key.md) | POST | Rotates an integration key in Svix. |
| [Update Integration](actions/update-integration.md) | PUT | Updates an integration in Svix. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a message in Svix. |
| [Create Message Precheck](actions/create-message-precheck.md) | POST | Checks active Svix endpoints before creating a message. |
| [Delete Message Payload](actions/delete-message-payload.md) | DELETE | Deletes a message payload from Svix. |
| [Expunge All Message Contents](actions/expunge-all-message-contents.md) | POST | Deletes all message payloads from a Svix application. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Svix. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from Svix. |
| [Poller Consumer Poll](actions/poller-consumer-poll.md) | GET | Retrieves polled messages for a Svix sink consumer. |
| [Poller Consumer Seek](actions/poller-consumer-seek.md) | POST | Sets a Svix sink consumer poller offset. |
| [Poller Poll](actions/poller-poll.md) | GET | Retrieves polled messages from a Svix sink. |

### Message Attempt

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attempt Response Body](actions/delete-attempt-response-body.md) | DELETE | Deletes an attempt response body from Svix. |
| [Get Attempt](actions/get-attempt.md) | GET | Retrieves a specific delivery attempt from Svix. |
| [List Attempted Destinations](actions/list-attempted-destinations.md) | GET | Retrieves attempted destinations for a specific Svix message. |
| [List Attempted Messages](actions/list-attempted-messages.md) | GET | Retrieves attempted messages for a specific Svix endpoint. |
| [List Attempts By Endpoint](actions/list-attempts-by-endpoint.md) | GET | Retrieves delivery attempts for a specific Svix endpoint. |
| [List Attempts By Msg](actions/list-attempts-by-msg.md) | GET | Retrieves delivery attempts for a specific Svix message. |
| [Resend Webhook](actions/resend-webhook.md) | POST | Resends a webhook to a specific Svix endpoint. |

### Sink

| Action | Method | Description |
| --- | --- | --- |
| [Create Sink](actions/create-sink.md) | POST | Creates a sink in Svix. |
| [Delete Sink](actions/delete-sink.md) | DELETE | Deletes a sink from Svix. |
| [Get Sink](actions/get-sink.md) | GET | Retrieves a sink from Svix. |
| [Get Sink Headers](actions/get-sink-headers.md) | GET | Retrieves sink headers from Svix. |
| [Get Sink Secret](actions/get-sink-secret.md) | GET | Retrieves a sink secret from Svix. |
| [Get Sink Transformation](actions/get-sink-transformation.md) | GET | Retrieves a sink transformation from Svix. |
| [List Sinks](actions/list-sinks.md) | GET | Retrieves sinks from Svix. |
| [Patch Sink](actions/patch-sink.md) | PUT | Updates a sink in Svix. |
| [Patch Sink Headers](actions/patch-sink-headers.md) | PUT | Updates sink headers in Svix. |
| [Rotate Sink Secret](actions/rotate-sink-secret.md) | POST | Rotates a sink secret in Svix. |
| [Set Sink Transformation](actions/set-sink-transformation.md) | PUT | Updates transformation code for a Svix sink. |
| [Update Sink](actions/update-sink.md) | PUT | Updates a sink in Svix. |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Aggregate App Stats](actions/aggregate-app-stats.md) | POST | Starts background aggregation of Svix application statistics. |
| [Aggregate Event Types](actions/aggregate-event-types.md) | PUT | Starts background aggregation of Svix event types. |

### Stream

| Action | Method | Description |
| --- | --- | --- |
| [Create Stream](actions/create-stream.md) | POST | Creates a stream in Svix. |
| [Delete Stream](actions/delete-stream.md) | DELETE | Deletes a stream from Svix. |
| [Get Stream](actions/get-stream.md) | GET | Retrieves a stream from Svix. |
| [List Streams](actions/list-streams.md) | GET | Retrieves streams from Svix. |
| [Patch Stream](actions/patch-stream.md) | PUT | Updates a stream in Svix. |
| [Update Stream](actions/update-stream.md) | PUT | Updates a stream in Svix. |

### Stream Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Get Poller Token](actions/get-poller-token.md) | GET | Retrieves the current Svix poller token. |
| [Get Stream Portal Access](actions/get-stream-portal-access.md) | POST | Retrieves stream portal access from Svix. |
| [Rotate Poller Token](actions/rotate-poller-token.md) | POST | Rotates the current Svix poller token. |
| [Stream Expire All](actions/stream-expire-all.md) | POST | Expires all stream tokens in Svix. |
| [Stream Logout](actions/stream-logout.md) | POST | Logs out a stream token in Svix. |

### Stream Event Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Stream Event Type](actions/create-stream-event-type.md) | POST | Creates a stream event type in Svix. |
| [Delete Stream Event Type](actions/delete-stream-event-type.md) | DELETE | Deletes a stream event type from Svix. |
| [Get Stream Event Type](actions/get-stream-event-type.md) | GET | Retrieves a stream event type from Svix. |
| [List Stream Event Types](actions/list-stream-event-types.md) | GET | Retrieves stream event types from Svix. |
| [Patch Stream Event Type](actions/patch-stream-event-type.md) | PUT | Updates a stream event type in Svix. |
| [Update Stream Event Type](actions/update-stream-event-type.md) | PUT | Creates or updates a stream event type in Svix. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Operational Webhook Endpoint](actions/create-operational-webhook-endpoint.md) | POST | Creates an operational webhook endpoint in Svix. |
| [Delete Operational Webhook Endpoint](actions/delete-operational-webhook-endpoint.md) | DELETE | Deletes an operational webhook endpoint from Svix. |
| [Get Operational Webhook Endpoint](actions/get-operational-webhook-endpoint.md) | GET | Retrieves an operational webhook endpoint from Svix. |
| [Get Operational Webhook Endpoint Headers](actions/get-operational-webhook-endpoint-headers.md) | GET | Retrieves operational webhook endpoint headers from Svix. |
| [Get Operational Webhook Endpoint Secret](actions/get-operational-webhook-endpoint-secret.md) | GET | Retrieves an operational webhook endpoint secret from Svix. |
| [List Operational Webhook Endpoints](actions/list-operational-webhook-endpoints.md) | GET | Retrieves operational webhook endpoints from Svix. |
| [Rotate Operational Webhook Endpoint Secret](actions/rotate-operational-webhook-endpoint-secret.md) | POST | Rotates an operational webhook endpoint secret in Svix. |
| [Update Operational Webhook Endpoint](actions/update-operational-webhook-endpoint.md) | PUT | Updates an operational webhook endpoint in Svix. |
| [Update Operational Webhook Endpoint Headers](actions/update-operational-webhook-endpoint-headers.md) | PUT | Updates operational webhook endpoint headers in Svix. |

