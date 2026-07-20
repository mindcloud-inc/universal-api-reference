# <img src="https://images.mindcloud.co/apps/icons/9l91ie9xth56_1781295192605.png" alt="Comm100 logo" width="28" height="28"> Comm100: Universal API

Comm100 is an AI-powered omnichannel customer service platform for live chat, ticketing, messaging, knowledge base, voice, and customer support operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/comm100/latest
- **Category:** Support / Contact Center
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.comm100.com
- **Vendor API docs:** https://developer.comm100.com/docs/server-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agent Statuses](actions/list-agent-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comm100/latest/actions/list-agent-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Statuses](actions/list-agent-statuses.md) | GET | Retrieves live chat agent statuses from Comm100. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a live chat campaign from Comm100. |
| [Get Campaign Chat Button](actions/get-campaign-chat-button.md) | GET | Retrieves campaign chat button settings from Comm100. |
| [Get Campaign Installation](actions/get-campaign-installation.md) | GET | Retrieves campaign installation details from Comm100. |
| [Get Campaign Manual Invitation](actions/get-campaign-manual-invitation.md) | GET | Retrieves a campaign manual invitation from Comm100. |
| [Get Campaign Pre-Chat](actions/get-campaign-pre-chat.md) | GET | Retrieves a campaign pre-chat form from Comm100. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves live chat campaigns from Comm100. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Private Canned Message Category](actions/get-private-canned-message-category.md) | GET | Retrieves a private canned message category from Comm100. |
| [Get Public Canned Message Category](actions/get-public-canned-message-category.md) | GET | Retrieves a public canned message category from Comm100. |
| [List Private Canned Message Categories](actions/list-private-canned-message-categories.md) | GET | Retrieves private canned message categories from Comm100. |
| [List Public Canned Message Categories](actions/list-public-canned-message-categories.md) | GET | Retrieves public canned message categories from Comm100. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Profile](actions/get-site-profile.md) | GET | Retrieves the site profile from Comm100 settings. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Search Chats](actions/search-chats.md) | GET | Searches live chat conversations in Comm100. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Permission](actions/get-permission.md) | GET | Retrieves a permission from Comm100 settings. |
| [Get Role Permissions](actions/get-role-permissions.md) | GET | Retrieves permissions for a role from Comm100 settings. |
| [List Permissions](actions/list-permissions.md) | GET | Retrieves global permissions from Comm100 settings. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from Comm100 settings. |
| [List Roles](actions/list-roles.md) | GET | Retrieves global roles from Comm100 settings. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Global Agent](actions/get-global-agent.md) | GET | Retrieves a global agent from Comm100 settings. |
| [List Global Agents](actions/list-global-agents.md) | GET | Retrieves global agents from Comm100 settings. |

