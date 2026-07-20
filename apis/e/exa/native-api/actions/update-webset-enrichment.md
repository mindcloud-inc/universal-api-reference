# Update Webset Enrichment with Exa

Updates an existing webset enrichment in Exa.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/websets/v0/websets/:webset/enrichments/:id`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Update Webset Enrichment](https://exa.ai/docs/websets/api/websets/enrichments/update-an-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | — |
| `id` | path | `string` | yes | — |
| `description` | body | `string` | no | Provide a description of the enrichment task you want to perform to each Webset Item. |
| `format` | body | `string` | no | Format of the enrichment response.  We automatically select the best format based on the description. If you want to explicitly specify the format, you can do so here. |
| `options[]` | body | `array<object>` | no | When the format is options, the different options for the enrichment agent to choose from. |
| `metadata` | body | `object` | no | Set of key-value pairs you want to associate with this object. |
