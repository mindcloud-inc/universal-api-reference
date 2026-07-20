# Get Deferred Chat Completion with xAI

Retrieves deferred chat completions from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/deferred-completion/:request_id`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Get Deferred Chat Completion](https://docs.x.ai/developers/rest-api-reference/inference/chat#get-deferred-chat-completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | no | Deferred request ID returned by a deferred chat completion. |
