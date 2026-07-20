# Get Deferred Chat Completions with Grok

Retrieves deferred chat completion results from Grok.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chat/deferred-completion/:request_id`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Get Deferred Chat Completions](https://docs.x.ai/developers/rest-api-reference/inference/chat#get-deferred-chat-completions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Deferred request identifier. |
