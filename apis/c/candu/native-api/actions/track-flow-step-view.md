# Track Flow Step View with Candu

Tracks a flow step view event in Candu.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventWebhook`
- **Base URL:** `https://api.candu.ai/api`
- **Official documentation:** [Track Flow Step View](https://developers.candu.ai/docs/eventing-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | The user ID the SDK event belongs to. |
| `properties` | body | `object` | yes | Required event-specific properties for the Candu flow step view event. |
| `timestamp` | body | `date` | no | Optional event timestamp. |
