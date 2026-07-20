# Get Webset Item with Exa

Retrieves a webset item from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/websets/v0/websets/:webset/items/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Get Webset Item](https://exa.ai/docs/websets/api/websets/items/get-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id or externalId of the Webset |
| `id` | path | `string` | yes | The id of the Webset item |
