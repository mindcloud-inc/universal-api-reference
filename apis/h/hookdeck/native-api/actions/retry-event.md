# Retry Event with Hookdeck

Retries an event in Hookdeck.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:id/retry`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Retry Event](https://hookdeck.com/docs/api/inspect.md#events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck event ID from the `id` path parameter. |
