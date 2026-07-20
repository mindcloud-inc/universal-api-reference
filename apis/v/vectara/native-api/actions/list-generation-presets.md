# List Generation Presets with Vectara

Retrieves available generation presets from Vectara.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/generation_presets`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [List Generation Presets](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `llm_name` | query | `string` | no | Filter generation presets by LLM name. |
| `limit` | query | `number` | no | Maximum number of presets to return. |
| `page_key` | query | `string` | no | Cursor for the next page of generation presets. |
