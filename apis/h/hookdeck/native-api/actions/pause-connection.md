# Pause Connection with Hookdeck

Pauses a connection in Hookdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/connections/:id/pause`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Pause Connection](https://hookdeck.com/docs/api/connections.md#pause-a-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck connection ID from the `id` path parameter. |
