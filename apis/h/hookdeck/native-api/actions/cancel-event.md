# Cancel Event with Hookdeck

Cancels a pending event in Hookdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:id/cancel`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Cancel Event](https://hookdeck.com/docs/api/inspect.md#events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck event ID from the `id` path parameter. |
