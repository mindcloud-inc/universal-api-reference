# Update Source with Hookdeck

Updates an existing source in Hookdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sources/:id`
- **Base URL:** `https://api.hookdeck.com/2025-07-01`
- **Official documentation:** [Update Source](https://hookdeck.com/docs/api/sources.md#update-a-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hookdeck source ID from the `id` path parameter. |
| `body` | body | `object` | yes | JSON request body for updating a Hookdeck source. Use the documented source update schema. |
