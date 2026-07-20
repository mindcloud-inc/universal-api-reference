# Retry Request with Hookdeck

Retries a request in Hookdeck.

## Endpoint

- **Method:** `POST`
- **Path:** `/requests/:id/retry`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Retry Request](https://hookdeck.com/docs/api/inspect.md#requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck request ID from the `id` path parameter. |
| `body` | body | `object` | yes | JSON request body for retrying a Hookdeck request. Use an empty object to consider all connection IDs, or provide `webhook_ids`. |
