# Update Connection with Hookdeck

Updates an existing connection in Hookdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/connections/:id`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Update Connection](https://hookdeck.com/docs/api/connections.md#update-a-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck connection ID from the `id` path parameter. |
| `body` | body | `object` | yes | JSON request body for updating a Hookdeck connection. Use the documented connection update schema. |
