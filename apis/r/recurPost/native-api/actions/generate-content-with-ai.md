# Generate Content with AI with RecurPost

Generates social content with AI in RecurPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate_content_with_ai`
- **Base URL:** `https://social.recurpost.com`
- **Official documentation:** [Generate Content with AI](https://developers.recurpost.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ai_id` | body | `string` | no | AI session ID for continuing a previous conversation. |
| `chat_history[]` | body | `array<object>` | no | Previous conversation messages with roles and content. |
| `chat_progress` | body | `string` | no | Progress marker returned by a previous AI response. |
| `prompt_text` | body | `string` | yes | Topic or text to generate content about. |
