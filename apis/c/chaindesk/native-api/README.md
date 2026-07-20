# Chaindesk: Native API Reference

A consolidated summary of Chaindesk's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.chaindesk.ai/api-reference
- **API base URL:** `https://app.chaindesk.ai/api`

## Authentication

### API Key

Authenticate with a Chaindesk API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.chaindesk.ai/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Continue Agent Conversation](actions/continue-agent-conversation.md) | `POST /agents/:agentId/query` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/agents/query) |
| [Create Agent](actions/create-agent.md) | `POST /agents` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Create Mail Inbox](actions/create-mail-inbox.md) | `POST /mail-inboxes` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Create Pinecone Datastore](actions/create-pinecone-datastore.md) | `POST /datastores` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Create Qdrant Datastore](actions/create-qdrant-datastore.md) | `POST /datastores` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Create S3 Datastore](actions/create-s3-datastore.md) | `POST /datastores` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Create Text Datasource](actions/create-text-datasource.md) | `POST /datasources` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/datasources/create) |
| [Create Web Page Datasource](actions/create-web-page-datasource.md) | `POST /datasources` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/datasources/create) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /agents/:agentId` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/agents/delete) |
| [Delete Datastore](actions/delete-datastore.md) | `DELETE /datastores/:datastoreId` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/datastores/delete) |
| [Delete Mail Inbox](actions/delete-mail-inbox.md) | `DELETE /mail-inboxes/:mailInboxId` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Get Agent](actions/get-agent.md) | `GET /agents/:agentId` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Get Conversation Messages](actions/get-conversation-messages.md) | `GET /conversations/:conversationId/messages` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/conversations/messages) |
| [Get Datasource](actions/get-datasource.md) | `GET /datasources/:datasourceId` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Get Datastore](actions/get-datastore.md) | `GET /datastores/:datastoreId` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Get Mail Inbox](actions/get-mail-inbox.md) | `GET /mail-inboxes/:mailInboxId` | [docs](https://docs.chaindesk.ai/api-reference) |
| [List Agent Conversations](actions/list-agent-conversations.md) | `GET /conversations` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/conversations/get) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://docs.chaindesk.ai/api-reference) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.chaindesk.ai/api-reference) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/conversations/get) |
| [List Datasources](actions/list-datasources.md) | `GET /datasources` | [docs](https://docs.chaindesk.ai/api-reference) |
| [List Datastore Datasources](actions/list-datastore-datasources.md) | `GET /datasources` | [docs](https://docs.chaindesk.ai/api-reference) |
| [List Datastores](actions/list-datastores.md) | `GET /datastores` | [docs](https://docs.chaindesk.ai/api-reference) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://docs.chaindesk.ai/api-reference) |
| [List Mail Inboxes](actions/list-mail-inboxes.md) | `GET /mail-inboxes` | [docs](https://docs.chaindesk.ai/api-reference) |
| [Query Agent](actions/query-agent.md) | `POST /agents/:agentId/query` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/agents/query) |
| [Update Agent](actions/update-agent.md) | `PATCH /agents/:agentId` | [docs](https://docs.chaindesk.ai/api-reference/endpoint/agents/update) |
| [Update Mail Inbox](actions/update-mail-inbox.md) | `PATCH /mail-inboxes/:mailInboxId` | [docs](https://docs.chaindesk.ai/api-reference) |
