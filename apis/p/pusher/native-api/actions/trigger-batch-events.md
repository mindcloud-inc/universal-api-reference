# Trigger Batch Events with Pusher

Triggers multiple events in Pusher.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/{appId}/batch_events`
- **Base URL:** `https://api-{cluster}.pusher.com`
- **Official documentation:** [Trigger Batch Events](https://pusher.com/docs/channels/library_auth_reference/rest-api/#post-batch-events-trigger-multiple-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch[]` | body | `array<object>` | yes | An array of event objects to publish in a single request, up to 10 events on multi-tenant clusters. |
