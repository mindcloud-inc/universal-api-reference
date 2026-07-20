# <img src="https://images.mindcloud.co/apps/icons/chatling_1774028982560.png" alt="Chatling logo" width="28" height="28"> Chatling: Universal API

Manage AI chatbots, contacts, conversations, and knowledge base content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatling/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chatling.ai
- **Vendor API docs:** https://docs.chatling.ai/api-reference/v2/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Settings](actions/list-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Ai Language

| Action | Method | Description |
| --- | --- | --- |
| [List AI Languages](actions/list-ai-languages.md) | GET | Retrieves AI languages from Chatling. |

### Ai Model

| Action | Method | Description |
| --- | --- | --- |
| [List AI Models](actions/list-ai-models.md) | GET | Retrieves AI models from Chatling. |

### Chatbot

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Chatbot](actions/duplicate-chatbot.md) | POST | Creates a duplicate chatbot in Chatling. |
| [List Chatbots](actions/list-chatbots.md) | GET | Retrieves chatbots from Chatling. |
| [Retrieve Chatbot](actions/retrieve-chatbot.md) | GET | Retrieves a chatbot from Chatling. |
| [Update Chatbot Settings](actions/update-chatbot-settings.md) | PUT | Updates chatbot settings in Chatling. |

### Chatbot Template

| Action | Method | Description |
| --- | --- | --- |
| [List Chatbot Templates](actions/list-chatbot-templates.md) | GET | Retrieves chatbot templates from Chatling. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Chatling. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Chatling. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Chatling. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Chat With Knowledge Base AI](actions/chat-with-knowledge-base-ai.md) | GET | Chats with Chatling's knowledge base AI. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Chatling. |
| [Retrieve Conversation](actions/retrieve-conversation.md) | GET | Retrieves a conversation from Chatling. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Chatling. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET | Retrieves conversation messages from Chatling. |
| [Rate AI Answer](actions/rate-ai-answer.md) | PUT | Rates an AI answer in Chatling. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Credits Usage](actions/get-ai-credits-usage.md) | GET | Retrieves AI credits usage from Chatling. |
| [Get Chatbots Usage](actions/get-chatbots-usage.md) | GET | Retrieves chatbot usage from Chatling. |
| [Get Email Credits Usage](actions/get-email-credits-usage.md) | GET | Retrieves email credits usage from Chatling. |
| [Get Knowledge Base Usage](actions/get-knowledge-base-usage.md) | GET | Retrieves knowledge base usage from Chatling. |
| [Get User Seats Usage](actions/get-user-seats-usage.md) | GET | Retrieves user seats usage from Chatling. |

### Project Settings

| Action | Method | Description |
| --- | --- | --- |
| [List Settings](actions/list-settings.md) | GET | Retrieves project settings from Chatling. |
| [Update Settings](actions/update-settings.md) | PUT | Updates project settings in Chatling. |

