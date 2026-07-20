# Track Event with Userflow

Tracks a user or group event in Userflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [Track Event](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The event name to track. |
| `user_id` | body | `string` | yes | The user associated with the event. |
| `attributes` | body | `object` | no | Optional event attributes. |
