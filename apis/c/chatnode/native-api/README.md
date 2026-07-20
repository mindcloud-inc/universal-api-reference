# Chatnode: Native API Reference

A consolidated summary of Chatnode's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.chatnode.ai/docs/developer-guides/api/quick-start
- **API base URL:** `https://api.public.chatnode.ai/v1`

## Authentication

### Chatnode API Key

Use a Chatnode API key from the API Access page to authenticate public API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.chatnode.ai/docs/developer-guides/api/authenticate-me)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate Me](actions/authenticate-me.md) | `GET auth_me` | [docs](https://www.chatnode.ai/docs/developer-guides/api/authenticate-me) |
| [Get Chat History](actions/get-chat-history.md) | `POST get-chats/:botId` | [docs](https://www.chatnode.ai/docs/developer-guides/api/get-chat-history) |
| [Get Leads](actions/get-leads.md) | `POST get-conversation-ids/:botId` | [docs](https://www.chatnode.ai/docs/developer-guides/api/get-leads) |
| [Send Message](actions/send-message.md) | `POST :botId` | [docs](https://www.chatnode.ai/docs/developer-guides/api/send-message) |
