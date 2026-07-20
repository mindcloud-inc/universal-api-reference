# Update Destination with Hookdeck

Updates an existing destination in Hookdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/destinations/:id`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Update Destination](https://hookdeck.com/docs/api/destinations.md#update-a-destination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck destination ID from the `id` path parameter. |
| `body` | body | `object` | yes | JSON request body for updating a Hookdeck destination. Use the documented destination update schema. |
