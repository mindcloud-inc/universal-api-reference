# Extract Entities From HTML Fragment via HTTP POST with Dandelion

Retrieves entities from an HTML fragment in Dandelion via HTTP POST.

## Endpoint

- **Method:** `POST`
- **Path:** `/datatxt/nex/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Extract Entities From HTML Fragment via HTTP POST](https://dandelion.eu/docs/api/datatxt/nex/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html_fragment` | query | `string` | yes | HTML Fragment to analyze. |
| `lang` | query | `string` | no | ISO 639-1 language code or auto. |
| `top_entities` | query | `number` | no | Number of top-ranked entities to include. |
| `min_confidence` | query | `number` | no | Discard entities below this confidence threshold. |
| `min_length` | query | `number` | no | Discard entities with spots shorter than this length. |
| `social.hashtag` | query | `boolean` | no | Parse hashtags as entities. |
| `social.mention` | query | `boolean` | no | Parse social mentions as entities. |
| `include` | query | `string` | no | Comma-separated list of extra fields to include. |
| `extra_types` | query | `string` | no | Comma-separated list of extra type providers. |
| `country` | query | `string` | no | Country code used for better disambiguation. |
