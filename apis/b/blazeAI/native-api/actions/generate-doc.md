# Generate Doc with Blaze AI

Creates an AI-generated document in Blaze AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspace_id/docs/ai-generation`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [Generate Doc](https://api.blaze.ai/api/documentation#!/docs/postApiV1WWorkspaceIdDocsAiGeneration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | Blaze workspace ID. |
| `prompt[prompt_text]` | body | `string` | yes | Prompt text for the new doc. |
| `prompt[generation_type]` | body | `string` | yes | Blaze generation mode. |
| `prompt[tone]` | body | `string` | yes | — |
| `prompt[seo_words]` | body | `string` | yes | — |
| `prompt[length]` | body | `string` | no | — |
| `prompt[brand_voice_id]` | body | `string` | no | — |
| `project_id` | body | `string` | no | — |
| `article_id` | body | `string` | no | — |
| `title` | body | `string` | no | Optional document title. |
| `mode` | body | `string` | no | — |
