# Track Event with Candu

Tracks a custom event for a Candu user.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventWebhook`
- **Base URL:** `https://api.candu.ai/api`
- **Official documentation:** [Track Event](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | The user ID the event belongs to. |
| `event` | body | `string` | yes | The custom event name to track. |
| `properties` | body | `object` | no | Optional event properties object. |
| `timestamp` | body | `date` | no | Optional event timestamp. |
