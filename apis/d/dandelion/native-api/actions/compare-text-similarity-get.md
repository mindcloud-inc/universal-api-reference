# Compare Text Similarity via HTTP GET with Dandelion

Retrieves text similarity from Dandelion via HTTP GET.

## Endpoint

- **Method:** `GET`
- **Path:** `/datatxt/sim/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Compare Text Similarity via HTTP GET](https://dandelion.eu/docs/api/datatxt/sim/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text1` | query | `string` | yes | First text to compare. |
| `text2` | query | `string` | yes | Second text to compare. |
| `lang` | query | `string` | no | Language code or auto-detect. |
| `bow` | query | `string` | no | Fallback strategy: never, both_empty, one_empty, or always. |
| `nex.min_confidence` | query | `number` | no | Optional prefixed Entity Extraction parameter. |
| `nex.top_entities` | query | `number` | no | Optional prefixed Entity Extraction parameter. |
| `nex.include` | query | `string` | no | Optional prefixed Entity Extraction include values as a comma-separated list. |
| `nex.extra_types` | query | `string` | no | Optional prefixed Entity Extraction extra types as a comma-separated list. |
