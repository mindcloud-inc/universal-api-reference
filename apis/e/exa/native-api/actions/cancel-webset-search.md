# Cancel Webset Search with Exa

Cancels a running webset search in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/websets/v0/websets/:webset/searches/:id/cancel`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Cancel Webset Search](https://exa.ai/docs/websets/api/websets/searches/cancel-a-running-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id of the Webset |
| `id` | path | `string` | yes | The id of the Search |
