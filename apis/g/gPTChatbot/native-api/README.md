# GPT Chatbot: Native API Reference

A consolidated summary of GPT Chatbot's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.gptchatbot.it/api-reference
- **API base URL:** `https://app.gptchatbot.it/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.gptchatbot.it/api-reference/api-key-setup)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /chatbot/:uuid/agent/create` | [docs](https://docs.gptchatbot.it/api-reference/agents/create) |
| [Create Chatbot](actions/create-chatbot.md) | `POST /chatbot/create` | [docs](https://docs.gptchatbot.it/api-reference/chatbots/create) |
| [Create Message](actions/create-message.md) | `POST /session/:uuid/message/stream` | [docs](https://docs.gptchatbot.it/api-reference/messages/create) |
| [Create QA Source](actions/create-qa-source.md) | `POST /chatbot/:uuid/data-source/qa` | [docs](https://docs.gptchatbot.it/api-reference/data-sources/create-qa) |
| [Create Session](actions/create-session.md) | `POST /chatbot/:uuid/session/create` | [docs](https://docs.gptchatbot.it/api-reference/sessions/create) |
| [Create URL Source](actions/create-url-source.md) | `POST /chatbot/:uuid/data-source/url` | [docs](https://docs.gptchatbot.it/api-reference/data-sources/create-url) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /agent/:uuid/delete` | [docs](https://docs.gptchatbot.it/api-reference/agents/delete) |
| [Delete Chatbot](actions/delete-chatbot.md) | `DELETE /chatbot/:uuid/delete` | [docs](https://docs.gptchatbot.it/api-reference/chatbots/delete) |
| [Delete Message](actions/delete-message.md) | `POST /message/:uuid/delete` | [docs](https://docs.gptchatbot.it/api-reference/messages/delete) |
| [Delete Session](actions/delete-session.md) | `POST /session/:uuid/delete` | [docs](https://docs.gptchatbot.it/api-reference/sessions/delete) |
| [Delete Source](actions/delete-source.md) | `POST /data-source/:uuid/delete` | [docs](https://docs.gptchatbot.it/api-reference/data-sources/delete) |
| [Get Chatbot](actions/get-chatbot.md) | `GET /chatbot/:uuid` | [docs](https://docs.gptchatbot.it/api-reference/chatbots/fetch) |
| [Get Session](actions/get-session.md) | `GET /session/:uuid` | [docs](https://docs.gptchatbot.it/api-reference/sessions/fetch) |
| [Get Session History](actions/get-session-history.md) | `GET /session/:uuid/messages/plain-text` | [docs](https://docs.gptchatbot.it/api-reference/messages/fetch-message-history) |
| [List Agents](actions/list-agents.md) | `GET /chatbot/:uuid/agents` | [docs](https://docs.gptchatbot.it/api-reference/agents/fetch_multi) |
| [List Chatbots](actions/list-chatbots.md) | `GET /chatbots` | [docs](https://docs.gptchatbot.it/api-reference/chatbots/fetch_multi) |
| [List Messages](actions/list-messages.md) | `GET /session/:uuid/messages` | [docs](https://docs.gptchatbot.it/api-reference/messages/fetch_multi) |
| [List Sessions](actions/list-sessions.md) | `GET /chatbot/:uuid/sessions` | [docs](https://docs.gptchatbot.it/api-reference/sessions/fetch_multi) |
| [List Sources](actions/list-sources.md) | `GET /chatbot/:uuid/data-sources` | [docs](https://docs.gptchatbot.it/api-reference/data-sources/fetch_multi) |
| [Retrain Sources](actions/retrain-sources.md) | `POST /data-sources/url/re-scrape` | [docs](https://docs.gptchatbot.it/api-reference/data-sources/retrain) |
| [Update Agent](actions/update-agent.md) | `POST /agent/:uuid/update` | [docs](https://docs.gptchatbot.it/api-reference/agents/update) |
| [Update Chatbot](actions/update-chatbot.md) | `POST /chatbot/:uuid/update` | [docs](https://docs.gptchatbot.it/api-reference/chatbots/update) |
| [Update Source](actions/update-source.md) | `POST /data-source/:uuid/update` | [docs](https://docs.gptchatbot.it/api-reference/data-sources/update) |
| [Upload File](actions/upload-file.md) | `POST /chatbot/:uuid/data-source/upload` | [docs](https://docs.gptchatbot.it/api-reference/data-sources/create-file) |
