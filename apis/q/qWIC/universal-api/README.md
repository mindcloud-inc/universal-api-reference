# <img src="https://images.mindcloud.co/apps/icons/qwic_1774981130769.png" alt="QWIC logo" width="28" height="28"> QWIC: Universal API

Automate sales, support, and marketing conversations with AI chatbots

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qWIC/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.qwic.ai
- **Vendor API docs:** https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Bot Flow](actions/fetch-bot-flow.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/fetch-bot-flow?connectionId=$CONNECTION_ID&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST | Creates a new bot in QWIC. |
| [Deploy Bot Flow](actions/deploy-bot-flow.md) | PUT | Deploys a flow for a QWIC bot. |
| [Fetch Bot Flow](actions/fetch-bot-flow.md) | GET | Retrieves the flow for a QWIC bot. |
| [List Bots](actions/list-bots.md) | GET | Retrieves bots from a QWIC account. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contacts](actions/create-contacts.md) | POST | Creates contacts in QWIC. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Close Conversation](actions/close-conversation.md) | PUT | Closes a QWIC conversation. |
| [Create SMS Conversation](actions/create-sms-conversation.md) | POST | Creates an SMS conversation in QWIC. |
| [Create WhatsApp Conversation](actions/create-whats-app-conversation.md) | POST | Creates a WhatsApp conversation in QWIC. |
| [Reassign Conversation To Agent](actions/reassign-conversation-to-agent.md) | PUT | Reassigns a QWIC conversation to an agent. |
| [Reassign Conversation To Team](actions/reassign-conversation-to-team.md) | PUT | Reassigns a QWIC conversation to a team. |
| [Send Agent Response to Conversation](actions/send-agent-response-to-conversation.md) | PUT | Sends an agent response to a QWIC conversation. |
| [Send Visitor Response](actions/send-visitor-response.md) | PUT | Sends a visitor response to a QWIC conversation. |
| [Start API Conversation](actions/start-api-conversation.md) | POST | Starts a conversation in QWIC through the API. |
| [Update Conversation Variables](actions/update-conversation-variables.md) | PUT | Updates variables for a QWIC conversation. |

### Events Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Set Events Webhook URL](actions/set-events-webhook-url.md) | PUT | Updates the events webhook URL in QWIC. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Add Knowledge Base Domain Data Source](actions/add-knowledge-base-domain-data-source.md) | POST | Adds a domain data source to a QWIC knowledge base. |
| [Add Knowledge Base Individual URL Data Sources](actions/add-knowledge-base-individual-url-data-sources.md) | POST | Adds webpage data sources to a QWIC knowledge base. |
| [Add Knowledge Base Text or File Data Sources](actions/add-knowledge-base-text-or-file-data-sources.md) | POST | Adds text or file data sources to a QWIC knowledge base. |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST | Creates a new knowledge base in QWIC. |
| [Fetch Knowledge Base Details](actions/fetch-knowledge-base-details.md) | GET | Retrieves details for a QWIC knowledge base. |
| [Get Data Source Training Status](actions/get-data-source-training-status.md) | GET | Retrieves training status for a QWIC data source. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET |  |

