# Generate email subject or body content using AI with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ai-assistant/generate`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Generate email subject or body content using AI](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Type of content to generate (subject or body) |
| `prompt` | body | `string` | yes | The prompt or context for the AI to use |
| `audience` | body | `string` | yes | The target audience for the email |
| `sender` | body | `string` | no | The sender persona for the email |
| `goal` | body | `string` | no | The goal of the email |
| `tone` | body | `string` | no | The tone of the email |
