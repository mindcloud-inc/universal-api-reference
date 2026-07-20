# Generate Business Response with Botsonic

Generates a business chatbot response in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/botsonic`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Generate Business Response](https://docs.botsonic.com/reference/generate_sync_or_streaming_response_v1_business_botsonic_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input_text` | body | `string` | yes | User question for the bot. |
| `chat_id` | body | `string` | yes | Chat identifier for the conversation. |
| `stream` | query | `boolean` | no | Set true to stream data; false for standard retrieval. |
| `source` | body | `string` | no | Optional sources for the bot to reference. |
| `starter_question_id` | body | `string` | no | Starter question identifier. |
| `is_business_api_request` | body | `boolean` | no | Whether this is a business API request. |
| `is_integration_request` | body | `boolean` | no | Whether this is an integration request. |
| `integration_user_identifier` | body | `string` | no | Integration user unique identifier. |
| `user_unique_identifier` | body | `string` | no | Additional user identifier stored with the inbox conversation. |
| `chat_history[]` | body | `array<object>` | no | Previous chat history for reference. |
| `chat_user_id` | body | `string` | no | Chat user identifier linked with existing user data. |
| `extra_metadata` | body | `object` | no | Additional metadata for the chat. |
| `full_history` | body | `boolean` | no | Return the full chat history when true. |
| `message_id` | body | `string` | no | Message identifier used to resolve handoff. |
| `timeout` | body | `number` | no | Maximum seconds to keep the connection open while generating a response. |
