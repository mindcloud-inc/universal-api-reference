# Sunshine Conversations: Native API Reference

A consolidated summary of Sunshine Conversations's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.zendesk.com/documentation/conversations/
- **OpenAPI specification:** https://raw.githubusercontent.com/zendesk/sunshine-conversations-api-spec/master/openapi.yaml
- **API base URL:** `https://api.smooch.io/v2`

## Authentication

### Basic Auth

Authenticate to Sunshine Conversations with an API key using HTTP Basic authentication. The key id is the username and the secret is the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **App ID:** `appId` · required · Sunshine Conversations app id used in API paths.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.zendesk.com/documentation/conversations/getting-started/api-authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page[size]` in the query string to set the page size (default 25; accepted range 1–100). Use `page[after]` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | `POST /apps/:appId/conversations` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Create User](actions/create-user.md) | `POST /apps/:appId/users` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /apps/:appId/conversations/:conversationId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Delete Message](actions/delete-message.md) | `DELETE /apps/:appId/conversations/:conversationId/messages/:messageId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Delete User](actions/delete-user.md) | `DELETE /apps/:appId/users/:userIdOrExternalId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Get App](actions/get-app.md) | `GET /apps/:appId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Get App Key](actions/get-app-key.md) | `GET /apps/:appId/keys/:keyId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Get Conversation](actions/get-conversation.md) | `GET /apps/:appId/conversations/:conversationId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Get Integration](actions/get-integration.md) | `GET /apps/:appId/integrations/:integrationId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Get User](actions/get-user.md) | `GET /apps/:appId/users/:userIdOrExternalId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List App Keys](actions/list-app-keys.md) | `GET /apps/:appId/keys` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Clients](actions/list-clients.md) | `GET /apps/:appId/users/:userIdOrExternalId/clients` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Conversations](actions/list-conversations.md) | `GET /apps/:appId/conversations` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Devices](actions/list-devices.md) | `GET /apps/:appId/users/:userIdOrExternalId/devices` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Integration Keys](actions/list-integration-keys.md) | `GET /apps/:appId/integrations/:integrationId/keys` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Integrations](actions/list-integrations.md) | `GET /apps/:appId/integrations` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Messages](actions/list-messages.md) | `GET /apps/:appId/conversations/:conversationId/messages` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Participants](actions/list-participants.md) | `GET /apps/:appId/conversations/:conversationId/participants` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Switchboards](actions/list-switchboards.md) | `GET /apps/:appId/switchboards` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /apps/:appId/integrations/:integrationId/webhooks` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Post Activity](actions/post-activity.md) | `POST /apps/:appId/conversations/:conversationId/activity` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Post Message](actions/post-message.md) | `POST /apps/:appId/conversations/:conversationId/messages` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /apps/:appId/conversations/:conversationId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
| [Update User](actions/update-user.md) | `PATCH /apps/:appId/users/:userIdOrExternalId` | [docs](https://developer.zendesk.com/api-reference/conversations/) |
