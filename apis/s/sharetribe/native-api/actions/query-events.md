# Query Events with Sharetribe

Retrieves events from Sharetribe.

## Endpoint

- **Method:** `GET`
- **Path:** `events/query`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Query Events](https://www.sharetribe.com/api-reference/integration.html#query-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startAfterSequenceId` | query | `number` | no | Return events after this sequence ID for forward-only pagination. |
| `createdAtStart` | query | `date` | no | Filter events created on or after this ISO 8601 timestamp. |
| `resourceId` | query | `string` | no | Return events related to this resource ID. |
| `relatedResourceId` | query | `string` | no | Return events related to this secondary resource ID. |
| `eventTypes` | query | `string` | no | Comma-separated list of event types to include. Send multiple values as a string separated by `,`. |
