# Compare HTML Fragment Similarity via HTTP POST with Dandelion

Retrieves HTML fragment similarity from Dandelion via HTTP POST.

## Endpoint

- **Method:** `POST`
- **Path:** `/datatxt/sim/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Compare HTML Fragment Similarity via HTTP POST](https://dandelion.eu/docs/api/datatxt/sim/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html_fragment1` | query | `string` | yes | First HTML fragment to compare. |
| `html_fragment2` | query | `string` | yes | Second HTML fragment to compare. |
| `lang` | query | `string` | no | Language code or auto-detect. |
| `bow` | query | `string` | no | Fallback strategy: never, both_empty, one_empty, or always. |
| `nex.min_confidence` | query | `number` | no | Optional prefixed Entity Extraction parameter. |
| `nex.top_entities` | query | `number` | no | Optional prefixed Entity Extraction parameter. |
| `nex.include` | query | `string` | no | Optional prefixed Entity Extraction include values as a comma-separated list. |
| `nex.extra_types` | query | `string` | no | Optional prefixed Entity Extraction extra types as a comma-separated list. |
