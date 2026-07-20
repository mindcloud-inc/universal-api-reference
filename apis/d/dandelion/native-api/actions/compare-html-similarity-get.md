# Compare HTML Similarity via HTTP GET with Dandelion

Retrieves HTML similarity from Dandelion via HTTP GET.

## Endpoint

- **Method:** `GET`
- **Path:** `/datatxt/sim/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Compare HTML Similarity via HTTP GET](https://dandelion.eu/docs/api/datatxt/sim/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html1` | query | `string` | yes | First HTML document to compare. |
| `html2` | query | `string` | yes | Second HTML document to compare. |
| `lang` | query | `string` | no | Language code or auto-detect. |
| `bow` | query | `string` | no | Fallback strategy: never, both_empty, one_empty, or always. |
| `nex.min_confidence` | query | `number` | no | Optional prefixed Entity Extraction parameter. |
| `nex.top_entities` | query | `number` | no | Optional prefixed Entity Extraction parameter. |
| `nex.include` | query | `string` | no | Optional prefixed Entity Extraction include values as a comma-separated list. |
| `nex.extra_types` | query | `string` | no | Optional prefixed Entity Extraction extra types as a comma-separated list. |
