# Update Conversation Model with Typesense

Updates a conversation model in Typesense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/models/{{modelId}}`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Update Conversation Model](https://typesense.org/docs/30.0/api/conversational-search-rag.html#managing-conversation-models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `object` | yes | Conversation model update JSON body. |
| `modelId` | path | `string` | yes | Conversation model ID. |
