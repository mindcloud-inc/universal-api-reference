# Generate Content (Tuned Model) with Gemini

Generates content with a tuned model in Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/tunedModels/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Generate Content (Tuned Model)](https://ai.google.dev/api/tuning#method:-tunedmodels.generatecontent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Tuned model token for this route. Use tuned model ID with operation suffix and no `tunedModels/` prefix (for example `my-model-id:generateContent`). |
| `contents[]` | body | `array<object>` | yes | Conversation content for the model. Required by Gemini. |
| `systemInstruction` | body | `object` | no | Optional system-level instruction content. |
| `generationConfig` | body | `object` | no | Optional generation controls such as temperature and max output tokens. |
| `safetySettings[]` | body | `array<object>` | no | Optional safety thresholds by harm category. |
| `tools[]` | body | `array<object>` | no | Optional tool declarations available to the model. |
| `toolConfig` | body | `object` | no | Optional tool execution configuration. |
| `cachedContent` | body | `string` | no | Optional cached content resource to ground generation. |
