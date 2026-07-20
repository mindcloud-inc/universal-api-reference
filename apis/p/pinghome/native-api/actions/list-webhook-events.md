# List Webhook Events with Pinghome

Retrieves webhook events from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/incident-query/v1/webhook/:id/events`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Webhook Events](https://docs.pinghome.io/incident-management/ruleset-management-and-event-handling/get-webhook-events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The webhook ID. |
| `last_received_at` | query | `string` | no | Optional cursor timestamp for pagination. |
| `limit` | query | `number` | no | Optional maximum number of webhook events to return. |
