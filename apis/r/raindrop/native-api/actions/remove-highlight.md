# Remove Highlight with Raindrop

## Endpoint

- **Method:** `PUT`
- **Path:** `/raindrop/:id`
- **Base URL:** `https://api.raindrop.io/rest/v1`
- **Official documentation:** [Remove Highlight](https://developer.raindrop.io/v1/highlights)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlights` | body | `string` | no | Array of highlight objects to remove. |
| `id` | path | `string` | no | Existing raindrop ID. |
