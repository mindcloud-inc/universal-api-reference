# DONNAJAMES Easy: Native API Reference

A consolidated summary of DONNAJAMES Easy's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://guide.gpt-trainer.com/api-reference/api-key-setup
- **API base URL:** `https://app.gpt-trainer.com/api/v1`

## Authentication

### API Key

Use a GPT-Trainer API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://guide.gpt-trainer.com/api-reference/api-key-setup)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST chatbot/:uuid/agent/create` | [docs](https://guide.gpt-trainer.com/api-reference/agents/create) |
| [Create Chatbot](actions/create-chatbot.md) | `POST chatbot/create` | [docs](https://guide.gpt-trainer.com/api-reference/chatbots/create) |
| [Create Message](actions/create-message.md) | `POST session/:uuid/message/stream` | [docs](https://guide.gpt-trainer.com/api-reference/messages/create) |
| [Create QA Source](actions/create-qa-source.md) | `POST chatbot/:uuid/data-source/qa` | [docs](https://guide.gpt-trainer.com/api-reference/data-sources/create-qa) |
| [Create Session](actions/create-session.md) | `POST chatbot/:uuid/session/create` | [docs](https://guide.gpt-trainer.com/api-reference/sessions/create) |
| [Create Source Tag](actions/create-source-tag.md) | `POST chatbot/:uuid/source-tag/create` | [docs](https://guide.gpt-trainer.com/api-reference/source-tags/create) |
| [Create URL Source](actions/create-url-source.md) | `POST chatbot/:uuid/data-source/url` | [docs](https://guide.gpt-trainer.com/api-reference/data-sources/create-url) |
| [Delete Agent](actions/delete-agent.md) | `DELETE agent/:uuid/delete` | [docs](https://guide.gpt-trainer.com/api-reference/agents/delete) |
| [Delete Chatbot](actions/delete-chatbot.md) | `DELETE chatbot/:uuid/delete` | [docs](https://guide.gpt-trainer.com/api-reference/chatbots/delete) |
| [Delete Message](actions/delete-message.md) | `POST message/:uuid/delete` | [docs](https://guide.gpt-trainer.com/api-reference/messages/delete) |
| [Delete Multiple Messages](actions/delete-multiple-messages.md) | `POST messages/delete` | [docs](https://guide.gpt-trainer.com/api-reference/messages/delete_multi) |
| [Delete Multiple Sources](actions/delete-multiple-sources.md) | `POST data-sources/delete` | [docs](https://guide.gpt-trainer.com/api-reference/data-sources/delete_multi) |
| [Delete Session](actions/delete-session.md) | `POST session/:uuid/delete` | [docs](https://guide.gpt-trainer.com/api-reference/sessions/delete) |
| [Delete Source](actions/delete-source.md) | `POST data-source/:uuid/delete` | [docs](https://guide.gpt-trainer.com/api-reference/data-sources/delete) |
| [Delete Source Tag](actions/delete-source-tag.md) | `DELETE source-tag/:uuid/delete` | [docs](https://guide.gpt-trainer.com/api-reference/source-tags/delete) |
| [Fetch a Chatbot](actions/fetch-a-chatbot.md) | `GET chatbot/:uuid` | [docs](https://guide.gpt-trainer.com/api-reference/chatbots/fetch) |
| [Fetch a Session](actions/fetch-a-session.md) | `GET session/:uuid` | [docs](https://guide.gpt-trainer.com/api-reference/sessions/fetch) |
| [Fetch All Agents](actions/fetch-all-agents.md) | `GET chatbot/:uuid/agents` | [docs](https://guide.gpt-trainer.com/api-reference/agents/fetch_multi) |
| [Fetch All Chatbots](actions/fetch-all-chatbots.md) | `GET chatbots` | [docs](https://guide.gpt-trainer.com/api-reference/chatbots/fetch_multi) |
| [Fetch All Messages](actions/fetch-all-messages.md) | `GET session/:uuid/messages` | [docs](https://guide.gpt-trainer.com/api-reference/messages/fetch_multi) |
| [Fetch All Sessions](actions/fetch-all-sessions.md) | `GET chatbot/:uuid/sessions` | [docs](https://guide.gpt-trainer.com/api-reference/sessions/fetch_multi) |
| [Fetch All Source Tags](actions/fetch-all-source-tags.md) | `GET chatbot/:uuid/source-tags` | [docs](https://guide.gpt-trainer.com/api-reference/source-tags/fetch-multi) |
| [Fetch List of Sources](actions/fetch-list-of-sources.md) | `GET chatbot/:uuid/data-sources` | [docs](https://guide.gpt-trainer.com/api-reference/data-sources/fetch_multi) |
| [Fetch Session History](actions/fetch-session-history.md) | `GET session/:uuid/messages/plain-text` | [docs](https://guide.gpt-trainer.com/api-reference/messages/fetch-message-history) |
| [Retrain Sources](actions/retrain-sources.md) | `POST data-sources/url/re-scrape` | [docs](https://guide.gpt-trainer.com/api-reference/data-sources/retrain) |
| [Update Agent](actions/update-agent.md) | `POST agent/:uuid/update` | [docs](https://guide.gpt-trainer.com/api-reference/agents/update) |
| [Update Chatbot](actions/update-chatbot.md) | `POST chatbot/:uuid/update` | [docs](https://guide.gpt-trainer.com/api-reference/chatbots/update) |
| [Update Source](actions/update-source.md) | `POST data-source/:uuid/update` | [docs](https://guide.gpt-trainer.com/api-reference/data-sources/update) |
| [Update Source Tag](actions/update-source-tag.md) | `POST source-tag/:uuid/update` | [docs](https://guide.gpt-trainer.com/api-reference/source-tags/update) |
