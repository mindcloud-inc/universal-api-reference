# Subscribe to Updates with LoopedIn

Subscribes a user to updates in LoopedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/updates/public-subscribe`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Subscribe to Updates](https://docs.loopedin.io/#subscribe-to-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The subscriber email address. |
| `name` | body | `string` | no | The subscriber name. |
| `workspace_id` | body | `string` | yes | The LoopedIn workspace ID. |
