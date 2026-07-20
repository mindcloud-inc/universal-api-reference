# Comm100: Native API Reference

A consolidated summary of Comm100's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.comm100.com/docs/server-api-reference
- **API base URL:** `https://api17.comm100.io/v4`

## Authentication

### API Key (Basic Auth)

Authenticate with the Comm100 agent email as the username and the Comm100 API key as the password. Comm100 also requires siteId on API requests when using API-key authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Site ID:** `siteId` · required · Comm100 site ID required on API requests when using API-key authentication.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.comm100.com/docs/server-api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | `GET livechat/campaigns/{{id}}` | [docs](https://developer.comm100.com/docs/server-api-livechat-campaign) |
| [Get Campaign Chat Button](actions/get-campaign-chat-button.md) | `GET livechat/campaigns/{{id}}/chatButton` | [docs](https://developer.comm100.com/docs/server-api-livechat-campaign) |
| [Get Campaign Installation](actions/get-campaign-installation.md) | `GET livechat/campaigns/{{id}}/installation` | [docs](https://developer.comm100.com/docs/server-api-livechat-installation) |
| [Get Campaign Manual Invitation](actions/get-campaign-manual-invitation.md) | `GET livechat/campaigns/{{id}}/manualInvitation` | [docs](https://developer.comm100.com/docs/server-api-livechat-campaign) |
| [Get Campaign Pre-Chat](actions/get-campaign-pre-chat.md) | `GET livechat/campaigns/{{id}}/preChat` | [docs](https://developer.comm100.com/docs/server-api-livechat-campaign) |
| [Get Global Agent](actions/get-global-agent.md) | `GET global/agents/{{id}}` | [docs](https://developer.comm100.com/docs/server-api-global-setting-agent) |
| [Get Permission](actions/get-permission.md) | `GET global/permissions/{{id}}` | [docs](https://developer.comm100.com/docs/server-api-global-setting-permission) |
| [Get Private Canned Message Category](actions/get-private-canned-message-category.md) | `GET global/privateCannedMessageCategories/{{id}}` | [docs](https://developer.comm100.com/docs/server-api-global-setting-private-canned-message-category) |
| [Get Public Canned Message Category](actions/get-public-canned-message-category.md) | `GET global/publicCannedMessageCategories/{{id}}` | [docs](https://developer.comm100.com/docs/server-api-global-setting-public-canned-message-category) |
| [Get Role](actions/get-role.md) | `GET global/roles/{{id}}` | [docs](https://developer.comm100.com/docs/server-api-global-setting-role) |
| [Get Role Permissions](actions/get-role-permissions.md) | `GET global/roles/{{id}}/permissions` | [docs](https://developer.comm100.com/docs/server-api-global-setting-permission) |
| [Get Site Profile](actions/get-site-profile.md) | `GET global/site` | [docs](https://developer.comm100.com/docs/server-api-global-setting-site-profile) |
| [List Agent Statuses](actions/list-agent-statuses.md) | `GET livechat/agents` | [docs](https://developer.comm100.com/docs/server-api-livechat-chat-server) |
| [List Campaigns](actions/list-campaigns.md) | `GET livechat/campaigns` | [docs](https://developer.comm100.com/docs/server-api-livechat-campaign) |
| [List Global Agents](actions/list-global-agents.md) | `GET global/agents` | [docs](https://developer.comm100.com/docs/server-api-global-setting-agent) |
| [List Permissions](actions/list-permissions.md) | `GET global/permissions` | [docs](https://developer.comm100.com/docs/server-api-global-setting-permission) |
| [List Private Canned Message Categories](actions/list-private-canned-message-categories.md) | `GET global/privateCannedMessageCategories` | [docs](https://developer.comm100.com/docs/server-api-global-setting-private-canned-message-category) |
| [List Public Canned Message Categories](actions/list-public-canned-message-categories.md) | `GET global/publicCannedMessageCategories` | [docs](https://developer.comm100.com/docs/server-api-global-setting-public-canned-message-category) |
| [List Roles](actions/list-roles.md) | `GET global/roles` | [docs](https://developer.comm100.com/docs/server-api-global-setting-role) |
| [Search Chats](actions/search-chats.md) | `POST livechat/chats\:Search` | [docs](https://developer.comm100.com/docs/server-api-livechat-chat) |
