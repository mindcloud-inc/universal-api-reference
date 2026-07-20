# Crisp: Native API Reference

A consolidated summary of Crisp's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.crisp.chat/references/rest-api/v1/
- **API base URL:** `https://api.crisp.chat/v1`

## Authentication

### Plugin Token

Authenticate with your Crisp plugin token identifier and key.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.crisp.chat/guides/rest-api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size. Use `page_number` in the request parameters to choose the page; numbering starts at 1.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Visitors](actions/count-visitors.md) | `GET /website/:website_id/visitors/count` | [docs](https://docs.crisp.chat/references/rest-api/v1/#count-visitors) |
| [Create New Conversation](actions/create-new-conversation.md) | `POST /website/:website_id/conversation` | [docs](https://docs.crisp.chat/references/rest-api/v1/#create-a-new-conversation) |
| [Get Connect Endpoints](actions/get-connect-endpoints.md) | `GET /plugin/connect/endpoints` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-connect-endpoints) |
| [Get Conversation](actions/get-conversation.md) | `GET /website/:website_id/conversation/:session_id` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-a-conversation) |
| [Get Conversation Metas](actions/get-conversation-metas.md) | `GET /website/:website_id/conversation/:session_id/meta` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-conversation-metas) |
| [Get Conversation Routing Assign](actions/get-conversation-routing-assign.md) | `GET /website/:website_id/conversation/:session_id/routing` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-conversation-routing-assign) |
| [Get Conversation State](actions/get-conversation-state.md) | `GET /website/:website_id/conversation/:session_id/state` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-conversation-state) |
| [Get Messages In Conversation](actions/get-messages-in-conversation.md) | `GET /website/:website_id/conversation/:session_id/messages` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-messages-in-conversation) |
| [Get People Data](actions/get-people-data.md) | `GET /website/:website_id/people/data/:people_id` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-people-data) |
| [Get People Profile](actions/get-people-profile.md) | `GET /website/:website_id/people/profile/:people_id` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-people-profile) |
| [Get People Statistics](actions/get-people-statistics.md) | `GET /website/:website_id/people/stats` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-people-statistics) |
| [Get Plugin Account](actions/get-plugin-account.md) | `GET /plugin/connect/account` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-connect-account) |
| [Get Verify Status For Conversation](actions/get-verify-status-for-conversation.md) | `GET /website/:website_id/conversation/:session_id/verify` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-verify-status-for-conversation) |
| [Get Website](actions/get-website.md) | `GET /website/:website_id` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-a-website) |
| [Get Website Availability Status](actions/get-website-availability-status.md) | `GET /website/:website_id/availability/status` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-website-availability-status) |
| [Get Website Operator](actions/get-website-operator.md) | `GET /website/:website_id/operator/:user_id` | [docs](https://docs.crisp.chat/references/rest-api/v1/#get-a-website-operator) |
| [List Connected Websites](actions/list-connected-websites.md) | `GET /plugin/connect/websites/all/:page_number` | [docs](https://docs.crisp.chat/references/rest-api/v1/#list-all-connect-websites) |
| [List Conversation Events](actions/list-conversation-events.md) | `GET /website/:website_id/conversation/:session_id/events/:page_number` | [docs](https://docs.crisp.chat/references/rest-api/v1/#list-conversation-events) |
| [List Conversation Files](actions/list-conversation-files.md) | `GET /website/:website_id/conversation/:session_id/files/:page_number` | [docs](https://docs.crisp.chat/references/rest-api/v1/#list-conversation-files) |
| [List Conversations](actions/list-conversations.md) | `GET /website/:website_id/conversations/:page_number` | [docs](https://docs.crisp.chat/references/rest-api/v1/#list-conversations) |
| [List People Profiles](actions/list-people-profiles.md) | `GET /website/:website_id/people/profiles/:page_number` | [docs](https://docs.crisp.chat/references/rest-api/v1/#list-people-profiles) |
| [List Visitors](actions/list-visitors.md) | `GET /website/:website_id/visitors/list/:page_number` | [docs](https://docs.crisp.chat/references/rest-api/v1/#list-visitors) |
| [List Website Operators](actions/list-website-operators.md) | `GET /website/:website_id/operators/list` | [docs](https://docs.crisp.chat/references/rest-api/v1/#list-website-operators) |
| [Remove Conversation](actions/remove-conversation.md) | `DELETE /website/:website_id/conversation/:session_id` | [docs](https://docs.crisp.chat/references/rest-api/v1/#remove-a-conversation) |
| [Resolve Helpdesk](actions/resolve-helpdesk.md) | `GET /website/:website_id/helpdesk` | [docs](https://docs.crisp.chat/references/rest-api/v1/#resolve-helpdesk) |
| [Send Message In Conversation](actions/send-message-in-conversation.md) | `POST /website/:website_id/conversation/:session_id/message` | [docs](https://docs.crisp.chat/references/rest-api/v1/#send-a-message-in-conversation) |
