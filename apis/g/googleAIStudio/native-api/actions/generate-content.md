# Generate Content with Google AI Studio

Generates content with a Gemini model in Google AI Studio.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Generate Content](https://ai.google.dev/api/generate-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example `gemini-2.5-flash:generateContent`. |
| `contents[]` | body | `array<object>` | yes | Conversation content for the model. Required by Gemini. |
| `systemInstruction` | body | `object` | no | Optional system-level instruction content. |
| `generationConfig` | body | `object` | no | Optional generation controls such as temperature and max output tokens. |
| `safetySettings[]` | body | `array<object>` | no | Optional safety thresholds by harm category. |
| `tools[]` | body | `array<object>` | no | Optional tool declarations available to the model. |
| `toolConfig` | body | `object` | no | Optional tool execution configuration. |
| `cachedContent` | body | `string` | no | Optional cached content resource to ground generation. |
