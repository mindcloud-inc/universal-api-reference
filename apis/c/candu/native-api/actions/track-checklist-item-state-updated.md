# Track Checklist Item State Updated with Candu

Tracks a checklist item state update event in Candu.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventWebhook`
- **Base URL:** `https://api.candu.ai/api`
- **Official documentation:** [Track Checklist Item State Updated](https://developers.candu.ai/docs/eventing-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | The user ID the SDK event belongs to. |
| `properties` | body | `object` | yes | Required event-specific properties for the Candu checklist item state update event. |
| `timestamp` | body | `date` | no | Optional event timestamp. |
