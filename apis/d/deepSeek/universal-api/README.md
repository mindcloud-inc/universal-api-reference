# <img src="https://images.mindcloud.co/apps/icons/deep-seek_1771964791170.png" alt="DeepSeek logo" width="28" height="28"> DeepSeek: Universal API

Generate text, reason through prompts, and build with DeepSeek models.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deepSeek/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deepseek.com
- **Vendor API docs:** https://api-docs.deepseek.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Chat Completions

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST |  |
| [Create Chat Prefix Completion (Beta)](actions/create-chat-prefix-completion-beta.md) | POST |  |

### Fim Completions

| Action | Method | Description |
| --- | --- | --- |
| [Create FIM Completion (Beta)](actions/create-fim-completion-beta.md) | POST |  |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET |  |

### User Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get User Balance](actions/get-user-balance.md) | GET |  |

