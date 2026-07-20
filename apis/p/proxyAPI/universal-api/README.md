# <img src="https://images.mindcloud.co/apps/icons/android-chrome-192x192_1776891386804.png" alt="ProxyAPI logo" width="28" height="28"> ProxyAPI: Universal API

Generate and analyze AI content with ProxyAPI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proxyAPI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://proxyapi.ru
- **Vendor API docs:** https://proxyapi.ru/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in ProxyAPI. |
| [Function-Calling Chat Completion](actions/function-calling-chat-completion.md) | POST | Creates a function-calling chat completion in ProxyAPI. |
| [Parallel Tool-Calling Chat](actions/parallel-tool-calling-chat.md) | POST | Creates a parallel tool-calling chat in ProxyAPI. |
| [Stream Chat Completion](actions/stream-chat-completion.md) | POST | Streams a chat completion from ProxyAPI. |
| [Structured Chat Completion](actions/structured-chat-completion.md) | POST | Creates a structured chat completion in ProxyAPI. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available models from ProxyAPI. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Custom-Tool Chat Completion](actions/custom-tool-chat-completion.md) | POST | Creates a custom-tool chat completion in ProxyAPI. |

