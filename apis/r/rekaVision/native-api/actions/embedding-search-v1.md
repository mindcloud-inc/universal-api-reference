# Embedding Search (V1) with Reka Vision

Finds video matches in Reka Vision by embedding query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/videos/search`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Embedding Search (V1)](https://docs.reka.ai/vision/api-reference/v-1/post-embedding-search)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `string` | yes |
| `threshold` | body | `number` | no |
| `max_results` | body | `number` | no |
| `video_ids[]` | body | `array<string>` | no |
| `group_ids[]` | body | `array<string>` | no |
| `search_demo` | body | `boolean` | no |
| `use_llm_rerank` | body | `boolean` | no |
| `use_embeds_rerank` | body | `boolean` | no |
| `add_ocr_to_caption` | body | `boolean` | no |
| `datetime_from` | body | `string` | no |
| `datetime_to` | body | `string` | no |
| `timestamp_from` | body | `number` | no |
| `timestamp_to` | body | `number` | no |
| `generate_report` | body | `boolean` | no |
