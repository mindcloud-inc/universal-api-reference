# Get Webset Enrichment with Exa

Retrieves a webset enrichment from Exa.

## Endpoint

- **Method:** `GET`
- **Path:** `/websets/v0/websets/:webset/enrichments/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Get Webset Enrichment](https://exa.ai/docs/websets/api/websets/enrichments/get-an-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id or externalId of the Webset |
| `id` | path | `string` | yes | The id of the Enrichment |
