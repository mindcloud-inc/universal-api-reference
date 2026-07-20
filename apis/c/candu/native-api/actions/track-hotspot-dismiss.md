# Track Hotspot Dismiss with Candu

Tracks a hotspot dismiss event in Candu.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventWebhook`
- **Base URL:** `https://api.candu.ai/api`
- **Official documentation:** [Track Hotspot Dismiss](https://developers.candu.ai/docs/eventing-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | The user ID the SDK event belongs to. |
| `properties` | body | `object` | yes | Required event-specific properties for the Candu hotspot dismiss event. |
| `timestamp` | body | `date` | no | Optional event timestamp. |
