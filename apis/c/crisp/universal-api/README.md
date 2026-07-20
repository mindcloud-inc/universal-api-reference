# <img src="https://images.mindcloud.co/apps/icons/crisp-icon_1776956153661.png" alt="Crisp logo" width="28" height="28"> Crisp: Universal API

Manage Crisp conversations, contacts, websites, and helpdesk content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crisp/latest
- **Category:** Communication / Team Messaging
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crisp.chat
- **Vendor API docs:** https://docs.crisp.chat/references/rest-api/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Plugin Account](actions/get-plugin-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crisp/latest/actions/get-plugin-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Connect Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Get Connect Endpoints](actions/get-connect-endpoints.md) | GET | Retrieves connect endpoints from Crisp. |

### Connected Website

| Action | Method | Description |
| --- | --- | --- |
| [List Connected Websites](actions/list-connected-websites.md) | GET | Retrieves connected websites from Crisp. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get People Profile](actions/get-people-profile.md) | GET | Retrieves a people profile from Crisp. |
| [List People Profiles](actions/list-people-profiles.md) | GET | Retrieves people profiles from Crisp. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Crisp. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Crisp. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create New Conversation](actions/create-new-conversation.md) | POST | Creates a new conversation in Crisp. |
| [Get Conversation Metas](actions/get-conversation-metas.md) | GET | Retrieves a conversation's metadata from Crisp. |
| [Get Conversation Routing Assign](actions/get-conversation-routing-assign.md) | GET | Retrieves a conversation's routing assignment from Crisp. |
| [Get Conversation State](actions/get-conversation-state.md) | GET | Retrieves a conversation's state from Crisp. |
| [Get Verify Status For Conversation](actions/get-verify-status-for-conversation.md) | GET | Retrieves a conversation's verify status from Crisp. |
| [Remove Conversation](actions/remove-conversation.md) | DELETE | Deletes an existing conversation from Crisp. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Events](actions/list-conversation-events.md) | GET | Retrieves events for a Crisp conversation. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Files](actions/list-conversation-files.md) | GET | Retrieves files for a Crisp conversation. |

### Helpdesk

| Action | Method | Description |
| --- | --- | --- |
| [Resolve Helpdesk](actions/resolve-helpdesk.md) | GET | Retrieves helpdesk information for a website in Crisp. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Messages In Conversation](actions/get-messages-in-conversation.md) | GET | Retrieves messages in a Crisp conversation. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Message In Conversation](actions/send-message-in-conversation.md) | POST | Sends a message in a Crisp conversation. |

### People Data

| Action | Method | Description |
| --- | --- | --- |
| [Get People Data](actions/get-people-data.md) | GET | Retrieves people data from Crisp. |

### People Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get People Statistics](actions/get-people-statistics.md) | GET | Retrieves people statistics from Crisp. |

### Plugin Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Plugin Account](actions/get-plugin-account.md) | GET | Retrieves your plugin account from Crisp. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Operator](actions/get-website-operator.md) | GET | Retrieves a website operator from Crisp. |
| [List Website Operators](actions/list-website-operators.md) | GET | Retrieves website operators from Crisp. |

### Visitor

| Action | Method | Description |
| --- | --- | --- |
| [List Visitors](actions/list-visitors.md) | GET | Retrieves visitors from Crisp. |

### Visitor Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Visitors](actions/count-visitors.md) | GET | Retrieves a visitor count from Crisp. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Get Website](actions/get-website.md) | GET | Retrieves a website from Crisp. |

### Website Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Availability Status](actions/get-website-availability-status.md) | GET | Retrieves website availability status from Crisp. |

