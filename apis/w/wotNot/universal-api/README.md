# <img src="https://images.mindcloud.co/apps/icons/wot-not_1774646287357.png" alt="WotNot logo" width="28" height="28"> WotNot: Universal API

Manage WotNot bots, conversations, contacts, and knowledge bases

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wotNot/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wotnot.io
- **Vendor API docs:** https://help.wotnot.io/build/integrations/public-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/list-bots?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST | Creates a new bot in WotNot. |
| [Deploy Bot Flow](actions/deploy-bot-flow.md) | PUT | Deploys a bot flow in WotNot. |
| [Get Bot Flow](actions/get-bot-flow.md) | GET | Retrieves a bot flow from WotNot. |
| [List Bots](actions/list-bots.md) | GET | Retrieves bots from WotNot. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Contact](actions/create-or-update-contact.md) | POST | Creates or updates a contact in WotNot. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Change Conversation Assignee To Team](actions/change-conversation-assignee-to-team.md) | PUT | Updates a conversation assignee to a team in WotNot. |
| [Change Conversation Assignee To User](actions/change-conversation-assignee-to-user.md) | PUT | Updates a conversation assignee to a user in WotNot. |
| [Close Conversation](actions/close-conversation.md) | PUT | Closes a conversation in WotNot. |
| [Start API Channel Conversation](actions/start-api-channel-conversation.md) | POST | Creates an API channel conversation in WotNot. |
| [Start SMS Conversation](actions/start-sms-conversation.md) | POST | Creates an SMS conversation in WotNot. |
| [Start WhatsApp Conversation](actions/start-whats-app-conversation.md) | POST | Creates a WhatsApp conversation in WotNot. |
| [Update Conversation Variables](actions/update-conversation-variables.md) | PUT | Updates conversation variables in WotNot. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Add Knowledge Base Domain Source](actions/add-knowledge-base-domain-source.md) | PUT | Adds a domain source to a WotNot knowledge base. |
| [Add Knowledge Base File Source](actions/add-knowledge-base-file-source.md) | PUT | Adds a file source to a WotNot knowledge base. |
| [Add Knowledge Base Text Source](actions/add-knowledge-base-text-source.md) | PUT | Adds a text source to a WotNot knowledge base. |
| [Add Knowledge Base Webpage Sources](actions/add-knowledge-base-webpage-sources.md) | PUT | Adds webpage sources to a WotNot knowledge base. |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST | Creates a knowledge base in WotNot. |
| [Delete Knowledge Base Data Sources](actions/delete-knowledge-base-data-sources.md) | DELETE | Deletes data sources from a WotNot knowledge base. |
| [Get Knowledge Base Data Source Training Status](actions/get-knowledge-base-data-source-training-status.md) | GET | Retrieves knowledge base source training status from WotNot. |
| [Get Knowledge Base Details](actions/get-knowledge-base-details.md) | GET | Retrieves a knowledge base from WotNot. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Agent File Response](actions/send-agent-file-response.md) | POST | Creates an agent file message in WotNot. |
| [Send Agent Template Response](actions/send-agent-template-response.md) | POST | Creates an agent template message in WotNot. |
| [Send Agent Text Response](actions/send-agent-text-response.md) | POST | Creates an agent text message in WotNot. |
| [Send Agent Voice Response](actions/send-agent-voice-response.md) | POST | Creates an agent voice message in WotNot. |
| [Send API Visitor Button Response](actions/send-api-visitor-button-response.md) | POST | Creates an API visitor button response in WotNot. |
| [Send API Visitor File Upload Response](actions/send-api-visitor-file-upload-response.md) | POST | Creates an API visitor file upload response in WotNot. |
| [Send API Visitor Multi-Button Response](actions/send-api-visitor-multi-button-response.md) | POST | Creates an API visitor multi-button response in WotNot. |
| [Send API Visitor Slider Response](actions/send-api-visitor-slider-response.md) | POST | Creates an API visitor slider response in WotNot. |
| [Send API Visitor Text Response](actions/send-api-visitor-text-response.md) | POST | Creates an API visitor text response in WotNot. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Set Events Webhook URL](actions/set-events-webhook-url.md) | PUT | Updates the events webhook URL in WotNot. |

