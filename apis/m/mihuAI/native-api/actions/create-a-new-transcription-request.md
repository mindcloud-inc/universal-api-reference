# Create a New Transcription Request with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/transcriptions`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Create a New Transcription Request](https://developers.mihu.ai/api-reference/transcriptions/create-a-new-transcription-request)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `coaching_agent_uuid` | body | `string` | no |
| `customer_email` | body | `string` | no |
| `customer_phone` | body | `string` | no |
| `email` | body | `string` | no |
| `possible_conversation` | body | `string` | no |
| `possible_language` | body | `string` | no |
| `qa_agent_uuid` | body | `string` | no |
| `reference_id` | body | `string` | no |
| `voice_url` | body | `string` | no |
| `webhook_header_token` | body | `string` | no |
| `webhook_url` | body | `string` | no |
