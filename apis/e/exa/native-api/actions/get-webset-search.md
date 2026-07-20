# Get Webset Search with Exa

Retrieves a webset search from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/websets/v0/websets/:webset/searches/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Get Webset Search](https://exa.ai/docs/websets/api/websets/searches/get-a-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id of the Webset |
| `id` | path | `string` | yes | The id of the Search |
