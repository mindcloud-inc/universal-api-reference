# Cancel Webset Enrichment with Exa

Cancels a running webset enrichment in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/websets/v0/websets/:webset/enrichments/:id/cancel`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Cancel Webset Enrichment](https://exa.ai/docs/websets/api/websets/enrichments/cancel-a-running-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id or externalId of the Webset |
| `id` | path | `string` | yes | The id of the Enrichment |
