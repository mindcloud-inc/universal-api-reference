# Chatvolt AI: Native API Reference

A consolidated summary of Chatvolt AI's API configuration and 107 documented operations, with links to official documentation.

- **Official docs:** https://docs.chatvolt.ai/introduction
- **OpenAPI specification:** https://docs.chatvolt.ai/introduction
- **API base URL:** `https://api.chatvolt.ai`

## Authentication

### API Key

Use a Chatvolt API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.chatvolt.ai/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (107 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Number to Whitelist](actions/agents-add-whitelist.md) | `POST /agent-whitelist-whatsapp` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/addWhitelist) |
| [Create Agent](actions/agents-create.md) | `POST /agents` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/create) |
| [Delete Agent](actions/agents-delete.md) | `DELETE /agents/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/delete) |
| [Delete Agent Blacklist Entry](actions/agents-delete-agent-blacklist-by-id.md) | `DELETE /agent-blacklist/{agentId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/delete-agent-blacklist-by-id) |
| [Delete Number from Whitelist](actions/agents-delete-whitelist.md) | `DELETE /agent-whitelist-whatsapp/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/deleteWhitelist) |
| [Get Agent](actions/agents-get.md) | `GET /agents/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/get) |
| [Get All Blacklist Entries](actions/agents-get-agent-blacklist.md) | `GET /agent-blacklist` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/get-agent-blacklist) |
| [Get Agent Blacklist by Agent ID](actions/agents-get-agent-blacklist-by-id.md) | `GET /agent-blacklist/{agentId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/get-agent-blacklist-by-id) |
| [Get Whitelist Numbers](actions/agents-get-whitelist.md) | `GET /agent-whitelist-whatsapp/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/getWhitelist) |
| [Update Number in Whitelist](actions/agents-patch-whitelist.md) | `PATCH /agent-whitelist-whatsapp/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/patchWhitelist) |
| [Add to Agent Blacklist](actions/agents-post-agent-blacklist.md) | `POST /agent-blacklist` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/post-agent-blacklist) |
| [Agent Query](actions/agents-query.md) | `POST /agents/{id}/query` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/query) |
| [Delete Tool](actions/agents-tools-delete.md) | `DELETE /api/agents/{agentId}/tools/{toolId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/tools/delete) |
| [Get Tools](actions/agents-tools-get.md) | `GET /api/agents/{agentId}/tools` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/tools/get) |
| [Update Tool](actions/agents-tools-patch.md) | `PATCH /api/agents/{agentId}/tools/{toolId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/tools/patch) |
| [Create Tool](actions/agents-tools-post.md) | `POST /api/agents/{agentId}/tools` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/tools/post) |
| [Update Agent](actions/agents-update.md) | `PATCH /agents/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/update) |
| [Enable/Disable Agent Integration](actions/agents-webhook.md) | `PATCH /agents/{id}/webhook` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/agents/webhook) |
| [Bulk Delete Artifacts](actions/artifacts-bulk-delete.md) | `DELETE /artifacts` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/bulk-delete) |
| [Create Category](actions/artifacts-categories-create.md) | `POST /artifact-categories` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/categories/create) |
| [Delete Category](actions/artifacts-categories-delete.md) | `DELETE /artifact-categories/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/categories/delete) |
| [Get Category](actions/artifacts-categories-get.md) | `GET /artifact-categories/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/categories/get) |
| [List Categories](actions/artifacts-categories-list.md) | `GET /artifact-categories` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/categories/list) |
| [Update Category](actions/artifacts-categories-update.md) | `PUT /artifact-categories/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/categories/update) |
| [Create Artifact](actions/artifacts-create.md) | `POST /artifacts` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/create) |
| [Delete/Toggle Artifact](actions/artifacts-delete.md) | `DELETE /artifacts/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/delete) |
| [Get Artifact](actions/artifacts-get.md) | `GET /artifacts/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/get) |
| [List Artifacts](actions/artifacts-list.md) | `GET /artifacts` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/list) |
| [Delete Media](actions/artifacts-media-delete.md) | `DELETE /artifacts/media/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/media/delete) |
| [List Media](actions/artifacts-media-list.md) | `GET /artifacts/media` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/media/list) |
| [Update Media](actions/artifacts-media-update.md) | `PATCH /artifacts/media/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/media/update) |
| [Upload Media](actions/artifacts-media-upload.md) | `POST /artifacts/media/upload` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/media/upload) |
| [Search Artifacts](actions/artifacts-search.md) | `GET /artifacts/search` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/search) |
| [Update Artifact](actions/artifacts-update.md) | `PUT /artifacts/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/update) |
| [Create or Update Contact](actions/contacts-create.md) | `POST /contacts` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/contacts/create) |
| [List Contacts](actions/contacts-get.md) | `GET /contacts` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/contacts/get) |
| [Assign to User](actions/conversation-assign.md) | `POST /conversations/{conversationId}/assign` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/assign) |
| [Create Note](actions/conversation-create-note.md) | `POST /conversations/{conversationId}/notes` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/create-note) |
| [Delete Conversation](actions/conversation-delete-conversation.md) | `DELETE /conversation/{conversationId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/delete-conversation) |
| [Delete Note](actions/conversation-delete-note.md) | `DELETE /conversations/{conversationId}/notes/{noteId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/delete-note) |
| [Delete Custom Variable](actions/conversation-delete-variable.md) | `DELETE /variables/{conversationId}/{varName}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/delete-variable) |
| [Get Conversation By Id](actions/conversation-get-by-id.md) | `GET /conversation/{conversationId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-by-id) |
| [Get Messages](actions/conversation-get-messages.md) | `GET /conversation/{conversationId}/messages/{count}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-messages) |
| [Get Notes](actions/conversation-get-notes.md) | `GET /conversations/{conversationId}/notes` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-notes) |
| [Get one Message](actions/conversation-get-one-message.md) | `GET /messages/{messageId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-one-message) |
| [Get One Custom Variable](actions/conversation-get-one-variable.md) | `GET /variables/{conversationId}/{varName}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-one-variable) |
| [Get All Custom Variables](actions/conversation-get-variables.md) | `GET /variables/{conversationId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-variables) |
| [List Conversations by Date](actions/conversation-list-by-date.md) | `GET /conversation` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/list-by-date) |
| [Register Message in Context](actions/conversation-message-register.md) | `POST /conversations/{conversationId}/message-register` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/message-register) |
| [Send Message by Channel](actions/conversation-send-message.md) | `POST /conversation/message/{type}/{value}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/send-message) |
| [Enable/Disable AI for Conversation](actions/conversation-set-ai-enabled.md) | `POST /conversations/{conversationId}/set-ai-enabled` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/set-ai-enabled) |
| [Set Priority](actions/conversation-set-priority.md) | `POST /conversations/{conversationId}/set-priority` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/set-priority) |
| [Update Note](actions/conversation-update-note.md) | `PUT /conversations/{conversationId}/notes/{noteId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/update-note) |
| [Update Status](actions/conversation-update-status.md) | `POST /conversations/{conversationId}/set-status` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/update-status) |
| [Create/Update Custom Variable](actions/conversation-upsert-variable.md) | `POST /variables` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/conversation/upsert-variable) |
| [Delete CRM Conversation Log](actions/crm-conversation-log-delete-crm-conversation-log.md) | `DELETE /crm/conversationLog/{logId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/conversation-log/delete-crm-conversation-log) |
| [Get CRM Conversation Log by ID](actions/crm-conversation-log-get-log-by-id.md) | `GET /crm/conversationLog/{logId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/conversation-log/get-log-by-id) |
| [List CRM Conversation Logs](actions/crm-conversation-log-list-crm-conversation-logs.md) | `GET /crm/conversationLog` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/conversation-log/list-crm-conversation-logs) |
| [Partially Update CRM Conversation Log](actions/crm-conversation-log-partially-update-crm-conversation-log.md) | `PATCH /crm/conversationLog/{logId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/conversation-log/partially-update-crm-conversation-log) |
| [Update CRM Conversation Log](actions/crm-conversation-log-update-crm-conversation-log.md) | `PUT /crm/conversationLog/{logId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/conversation-log/update-crm-conversation-log) |
| [Create CRM Scenario](actions/crm-scenario-create-scenario.md) | `POST /crm/scenario` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/create-scenario) |
| [Delete CRM Scenario](actions/crm-scenario-delete-scenario.md) | `DELETE /crm/scenario` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/delete-scenario) |
| [Remove Conversation from CRM Scenario](actions/crm-scenario-delete-scenario-conversation.md) | `DELETE /crm/scenario/{scenarioId}/conversation` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/delete-scenario-conversation) |
| [List Scenario Conversations](actions/crm-scenario-list-scenario-conversations.md) | `GET /crm/scenario/{scenarioId}/conversation` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/list-scenario-conversations) |
| [List CRM Scenarios](actions/crm-scenario-list-scenarios.md) | `GET /crm/scenario` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/list-scenarios) |
| [Update CRM Scenario](actions/crm-scenario-update-scenario.md) | `PUT /crm/scenario` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/update-scenario) |
| [Add Conversation to CRM Step](actions/crm-step-add-step-conversation.md) | `POST /crm/step/conversation` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/add-step-conversation) |
| [Create CRM Step](actions/crm-step-create-step.md) | `POST /crm/step` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/create-step) |
| [Delete CRM Step](actions/crm-step-delete-step.md) | `DELETE /crm/step` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/delete-step) |
| [List CRM Steps](actions/crm-step-list-steps.md) | `GET /crm/step` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/list-steps) |
| [Move Conversation to CRM Step](actions/crm-step-move-step.md) | `POST /crm/step/move` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/move-step) |
| [Update CRM Step](actions/crm-step-update-step.md) | `PUT /crm/step` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/update-step) |
| [Create Datasource](actions/datasources-create.md) | `POST /datasources` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datasources/create) |
| [Delete Datasource](actions/datasources-delete.md) | `DELETE /datasources/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datasources/delete) |
| [Get Datasource](actions/datasources-get.md) | `GET /datasources/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datasources/get) |
| [List Datasources](actions/datasources-list.md) | `GET /datasources/list` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datasources/list) |
| [Create Datastore](actions/datastores-create.md) | `POST /datastores` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datastores/create) |
| [Delete Datastore](actions/datastores-delete.md) | `DELETE /datastores/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datastores/delete) |
| [Get Datastore](actions/datastores-get.md) | `GET /datastores/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datastores/get) |
| [List Datastores](actions/datastores-list.md) | `GET /datastores/list` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datastores/list) |
| [Query Datastore](actions/datastores-query.md) | `POST /datastores/{id}/query` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datastores/query) |
| [Update Datastore](actions/datastores-update.md) | `PATCH /datastores/{id}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/datastores/update) |
| [Get Contact by ID](actions/dispatches-contacts-get-by-id.md) | `GET /dispatches/contacts/{contactId}` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/get-by-id) |
| [Unlink Contact from Dispatch](actions/dispatches-contacts-link-delete.md) | `DELETE /dispatches/contacts/link` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/link/delete) |
| [Get Contact Links](actions/dispatches-contacts-link-get.md) | `GET /dispatches/contacts/link` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/link/get) |
| [Link Contact to Dispatch](actions/dispatches-contacts-link-post.md) | `POST /dispatches/contacts/link` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/link/post) |
| [Delete a Contact List](actions/dispatches-contacts-lists-delete.md) | `DELETE /dispatches/contacts/lists` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/lists/delete) |
| [Get Contact Lists](actions/dispatches-contacts-lists-get.md) | `GET /dispatches/contacts/lists` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/lists/get) |
| [Create or Update a Contact List](actions/dispatches-contacts-lists-post.md) | `POST /dispatches/contacts/lists` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/lists/post) |
| [Edit Contact List](actions/dispatches-contacts-lists-put.md) | `PUT /dispatches/contacts/lists` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/lists/put) |
| [Create or Update Dispatch](actions/dispatches-create.md) | `POST /dispatches` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/create) |
| [Delete Scheduled Dispatch](actions/dispatches-delete.md) | `DELETE /dispatches` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/delete) |
| [List Dispatches](actions/dispatches-get.md) | `GET /dispatches` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/get) |
| [Populate Dispatch Queue](actions/dispatches-populate-queue.md) | `POST /dispatches/{id}/populate-queue` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/populate-queue) |
| [Get Mercado Livre Products](actions/mercadolivre-get-products.md) | `GET /mercadolivre/get-products` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/mercadolivre/get-products) |
| [Send SMS Message](actions/twilio-send-message.md) | `POST /twilio/{ownerPhone}/{contactPhone}/message` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/twilio/send-message) |
| [Create Meta Template](actions/whatsapp-create-template.md) | `POST /whatsapp/templates` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/create-template) |
| [List Meta Templates](actions/whatsapp-list-templates.md) | `GET /whatsapp/templates` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/list-templates) |
| [Location Request](actions/whatsapp-location-request.md) | `POST /messages/interactive/location-request` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/location-request) |
| [Send Buttons](actions/whatsapp-send-buttons.md) | `POST /messages/interactive/send-buttons` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-buttons) |
| [Send Contact](actions/whatsapp-send-contact.md) | `POST /messages/interactive/send-contact` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-contact) |
| [Send CTA](actions/whatsapp-send-cta.md) | `POST /messages/interactive/send-cta` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-cta) |
| [Send List](actions/whatsapp-send-lists.md) | `POST /messages/interactive/send-lists` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-lists) |
| [Send Location](actions/whatsapp-send-location.md) | `POST /messages/interactive/send-location` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-location) |
| [WhatsApp Template Message](actions/whatsapp-template-message.md) | `POST /whatsapp/{phoneNumberId}/template-message` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/template-message) |
| [Send WhatsApp Message](actions/zapi-zapi-send-whatsapp-message.md) | `POST /zapi/{instanceId}/{contactPhone}/message` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/zapi/zapi-send-whatsapp-message) |
| [Send a message through the Zapper integration](actions/zapper-send-message.md) | `POST /zapper/instances/{id}/message` | [docs](https://docs.chatvolt.ai/api-reference/endpoint/zapper/send-message) |
