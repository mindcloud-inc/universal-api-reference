# Unsubscribe from Updates with LoopedIn

Unsubscribes a user from updates in LoopedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/updates/public-unsubscribe`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Unsubscribe from Updates](https://docs.loopedin.io/#unsubscribe-from-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The subscriber email address. |
| `workspace_id` | body | `string` | yes | The LoopedIn workspace ID. |
