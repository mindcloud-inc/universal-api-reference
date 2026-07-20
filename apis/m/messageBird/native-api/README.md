# MessageBird: Native API Reference

A consolidated summary of MessageBird's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://docs.bird.com/api
- **OpenAPI specification:** https://global--openapi-specs--151603429280--use1.s3.us-east-1.amazonaws.com/joined-specs/openapi.yml
- **API base URL:** `https://api.bird.com`

## Authentication

### API Key

Use a Bird access key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.bird.com/api/api-access/api-authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `pageToken` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Allow/Block Rules in Bulk](actions/add-allowblock-rules-in-bulk.md) | `POST /workspaces/:workspaceId/conversation-allowblock-rules-bulk` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/add-allow-block-rules-in-bulk) |
| [Add Conversation Participant](actions/add-conversation-participant.md) | `POST /workspaces/:workspaceId/conversations/:conversationId/participants` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/add-participant-to-conversation) |
| [Create Allow/Block Rule](actions/create-allowblock-rule.md) | `POST /workspaces/:workspaceId/conversation-allowblock-rules` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/create-allow-block-rule) |
| [Create Conversation](actions/create-conversation.md) | `POST /workspaces/:workspaceId/conversations` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-management/create-conversation) |
| [Create Conversation Message](actions/create-conversation-message.md) | `POST /workspaces/:workspaceId/conversations/:conversationId/messages` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/create-conversation-message) |
| [Create Navigator](actions/create-navigator.md) | `POST /workspaces/:workspaceId/navigators` | [docs](https://docs.bird.com/api/channels-api/api-reference/navigators) |
| [Create Pre-Signed Upload](actions/create-pre-signed-upload.md) | `POST /workspaces/:workspaceId/conversations/:conversationId/presigned-upload` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/create-pre-signed-upload) |
| [Create Workspace](actions/create-workspace.md) | `POST /organizations/:organizationId/workspaces` | [docs](https://docs.bird.com/api/accounts-api/api-reference/organizations/workspaces) |
| [Delete Allow/Block Rule](actions/delete-allowblock-rule.md) | `DELETE /workspaces/:workspaceId/conversation-allowblock-rules/:allowBlockRuleId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/delete-allow-block-rule) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /workspaces/:workspaceId/conversations/:conversationId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-management/delete-conversation) |
| [Delete Conversation Message](actions/delete-conversation-message.md) | `DELETE /workspaces/:workspaceId/conversations/:conversationId/messages/:messageId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/delete-conversation-message) |
| [Delete Conversation Participant](actions/delete-conversation-participant.md) | `DELETE /workspaces/:workspaceId/conversations/:conversationId/participants/:conversationParticipantId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/delete-participant) |
| [Delete Navigator](actions/delete-navigator.md) | `DELETE /workspaces/:workspaceId/navigators/:navigatorId` | [docs](https://docs.bird.com/api/channels-api/api-reference/navigators) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /organizations/:organizationId/workspaces/:workspaceId` | [docs](https://docs.bird.com/api/accounts-api/api-reference/organizations/workspaces) |
| [Get Allow/Block Bulk Upload Status](actions/get-allowblock-bulk-upload-status.md) | `GET /workspaces/:workspaceId/conversation-allowblock-rules-bulk/:bulkId/status` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/get-allow-block-bulk-upload-status) |
| [Get Allow/Block Rule](actions/get-allowblock-rule.md) | `GET /workspaces/:workspaceId/conversation-allowblock-rules/:allowBlockRuleId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/get-allow-block-rule) |
| [Get Balance](actions/get-balance.md) | `GET /balance` | [docs](https://developers.messagebird.com/api/balance/) |
| [Get Channel](actions/get-channel.md) | `GET /workspaces/:workspaceId/channels/:channelId` | [docs](https://docs.bird.com/api/channels-api/api-reference/channels-management) |
| [Get Channel Details for a Contact](actions/get-channel-details-for-a-contact.md) | `GET /workspaces/:workspaceId/channels/:channelId/contacts/:contactId` | [docs](https://docs.bird.com/api/channels-api/api-reference/channels-management) |
| [Get Channel Message](actions/get-channel-message.md) | `GET /workspaces/:workspaceId/channels/:channelId/messages/:messageId` | [docs](https://docs.bird.com/api/channels-api/api-reference/messaging) |
| [Get Conversation](actions/get-conversation.md) | `GET /workspaces/:workspaceId/conversations/:conversationId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-management/get-conversation) |
| [Get Conversation Message](actions/get-conversation-message.md) | `GET /workspaces/:workspaceId/conversations/:conversationId/messages/:messageId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/get-conversation-message) |
| [Get Conversation Participant](actions/get-conversation-participant.md) | `GET /workspaces/:workspaceId/conversations/:conversationId/participants/:conversationParticipantId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/get-participant-by-id) |
| [Get Conversation Participant by Identifier](actions/get-conversation-participant-by-identifier.md) | `GET /workspaces/:workspaceId/conversations/:conversationId/participants/:identifierKey/:identifierValue` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/get-participant-by-identifier-key-and-value) |
| [Get Conversations Configuration](actions/get-conversations-configuration.md) | `GET /workspaces/:workspaceId/channels/:channelId/conversational` | [docs](https://docs.bird.com/api/conversations-api/api-reference/channel-configuration/get-conversations-configuration) |
| [Get Navigator](actions/get-navigator.md) | `GET /workspaces/:workspaceId/navigators/:navigatorId` | [docs](https://docs.bird.com/api/channels-api/api-reference/navigators) |
| [Get Navigator Coverage](actions/get-navigator-coverage.md) | `GET /workspaces/:workspaceId/navigators/:navigatorId/coverage` | [docs](https://docs.bird.com/api/channels-api/api-reference/navigators) |
| [Get Workspace](actions/get-workspace.md) | `GET /organizations/:organizationId/workspaces/:workspaceId` | [docs](https://docs.bird.com/api/accounts-api/api-reference/organizations/workspaces) |
| [List Allow/Block Rules](actions/list-allowblock-rules.md) | `GET /workspaces/:workspaceId/conversation-allowblock-rules` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/list-allow-block-rules) |
| [List Channel Messages](actions/list-channel-messages.md) | `GET /workspaces/:workspaceId/channels/:channelId/messages` | [docs](https://docs.bird.com/api/channels-api/api-reference/messaging) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /workspaces/:workspaceId/conversations/:conversationId/messages` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/list-conversation-messages) |
| [List Conversation Participants](actions/list-conversation-participants.md) | `GET /workspaces/:workspaceId/conversations/:conversationId/participants` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/list-participants) |
| [List Conversations](actions/list-conversations.md) | `GET /workspaces/:workspaceId/conversations` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-management/list-conversations) |
| [List Message Interactions](actions/list-message-interactions.md) | `GET /workspaces/:workspaceId/channels/:channelId/messages/:messageId/interactions` | [docs](https://docs.bird.com/api/channels-api/api-reference/messaging) |
| [List Navigators](actions/list-navigators.md) | `GET /workspaces/:workspaceId/navigators` | [docs](https://docs.bird.com/api/channels-api/api-reference/navigators) |
| [List Participant Conversations](actions/list-participant-conversations.md) | `GET /workspaces/:workspaceId/participants/:conversationParticipantId/conversations` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/list-participant-conversations-by-id) |
| [List Participant Conversations by Identifier](actions/list-participant-conversations-by-identifier.md) | `GET /workspaces/:workspaceId/participants/:identifierKey/:identifierValue/conversations` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/list-participant-conversations-by-identifier-key-and-value) |
| [List Workspace Channels](actions/list-workspace-channels.md) | `GET /workspaces/:workspaceId/channels` | [docs](https://docs.bird.com/api/channels-api/api-reference/channels-management) |
| [List Workspace Messages](actions/list-workspace-messages.md) | `GET /workspaces/:workspaceId/channels/messages` | [docs](https://docs.bird.com/api/channels-api/api-reference/messaging) |
| [List Workspaces](actions/list-workspaces.md) | `GET /organizations/:organizationId/workspaces` | [docs](https://docs.bird.com/api/accounts-api/api-reference/organizations/workspaces) |
| [Send Navigator Message](actions/send-navigator-message.md) | `POST /workspaces/:workspaceId/navigators/:navigatorId/messages` | [docs](https://docs.bird.com/api/channels-api/api-reference/navigators) |
| [Update Allow/Block Rule](actions/update-allowblock-rule.md) | `PATCH /workspaces/:workspaceId/conversation-allowblock-rules/:allowBlockRuleId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/update-allow-block-rule) |
| [Update Antispam Setting](actions/update-antispam-setting.md) | `PATCH /workspaces/:workspaceId/conversations-antispam-settings` | [docs](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/update-antispam-setting) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /workspaces/:workspaceId/conversations/:conversationId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-management/update-conversation) |
| [Update Conversation Message](actions/update-conversation-message.md) | `PATCH /workspaces/:workspaceId/conversations/:conversationId/messages/:messageId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/update-conversation-message) |
| [Update Conversation Participant](actions/update-conversation-participant.md) | `PATCH /workspaces/:workspaceId/conversations/:conversationId/participants/:conversationParticipantId` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/update-participant-by-id) |
| [Update Conversation Participant by Identifier](actions/update-conversation-participant-by-identifier.md) | `PATCH /workspaces/:workspaceId/conversations/:conversationId/participants/:identifierKey/:identifierValue` | [docs](https://docs.bird.com/api/conversations-api/api-reference/conversation-participants/update-participant-by-v-key-and-value) |
| [Update Conversations Configuration](actions/update-conversations-configuration.md) | `PATCH /workspaces/:workspaceId/channels/:channelId/conversational` | [docs](https://docs.bird.com/api/conversations-api/api-reference/channel-configuration/update-conversations-configuration) |
| [Update Navigator](actions/update-navigator.md) | `PATCH /workspaces/:workspaceId/navigators/:navigatorId` | [docs](https://docs.bird.com/api/channels-api/api-reference/navigators) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /organizations/:organizationId/workspaces/:workspaceId` | [docs](https://docs.bird.com/api/accounts-api/api-reference/organizations/workspaces) |
