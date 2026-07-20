# Delete Webset Enrichment with Exa

Deletes an existing webset enrichment from Exa.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/websets/v0/websets/:webset/enrichments/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Delete Webset Enrichment](https://exa.ai/docs/websets/api/websets/enrichments/delete-an-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id or externalId of the Webset |
| `id` | path | `string` | yes | The id of the Enrichment |
