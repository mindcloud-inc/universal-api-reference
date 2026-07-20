# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-famulor-io-48x48_1778173241207.png" alt="Famulor AI - Voice Agent logo" width="28" height="28"> Famulor AI - Voice Agent: Universal API

Famulor AI - Voice Agent lets teams manage AI phone assistants, calls, campaigns, leads, knowledge bases, phone numbers, chat conversations, SMS, SIP trunks, WhatsApp messaging, and account data through Famulor's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/famulorAIVoiceAgent/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.famulor.io/en
- **Vendor API docs:** https://docs.famulor.io/en/api-reference/introduction.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Call](actions/get-call.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/get-call?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Ai Reply

| Action | Method | Description |
| --- | --- | --- |
| [Generate AI Reply](actions/generate-ai-reply.md) | POST | Generates an AI reply in Famulor by customer identifier. |

### Assistant

| Action | Method | Description |
| --- | --- | --- |
| [Create Assistant](actions/create-assistant.md) | POST | Creates a new AI assistant in Famulor. |
| [Delete Assistant](actions/delete-assistant.md) | DELETE | Deletes an existing AI assistant from Famulor. |
| [Get Outbound Assistants](actions/get-outbound-assistants.md) | GET | Retrieves outbound assistants from Famulor. |
| [List Assistants](actions/list-assistants.md) | GET | Retrieves assistants from Famulor. |
| [Update Assistant](actions/update-assistant.md) | PUT | Updates an existing AI assistant in Famulor. |

### Assistant Inbound Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Disable Assistant Inbound Webhook](actions/disable-assistant-inbound-webhook.md) | PUT | Disables inbound webhook notifications for a Famulor assistant. |
| [Enable Assistant Inbound Webhook](actions/enable-assistant-inbound-webhook.md) | PUT | Enables inbound webhook notifications for a Famulor assistant. |

### Assistant Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Disable Assistant Webhook](actions/disable-assistant-webhook.md) | PUT | Disables webhook notifications for a Famulor assistant. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Delete Call](actions/delete-call.md) | DELETE | Deletes an existing call from Famulor. |
| [Get Call](actions/get-call.md) | GET | Retrieves call details from Famulor. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from Famulor. |
| [Make a Call](actions/make-call.md) | POST | Creates a new call in Famulor with a specific assistant. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new outbound campaign in Famulor. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Famulor. |
| [Update Campaign Status](actions/update-campaign-status.md) | PUT | Starts, pauses, or stops a campaign in Famulor. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in Famulor. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves conversation history from Famulor. |

### Conversation Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Conversation Message](actions/send-conversation-message.md) | POST | Sends a message to a Famulor conversation and returns the reply. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST | Creates a new knowledge base in Famulor. |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | DELETE | Deletes an existing knowledge base from Famulor. |
| [Get Knowledge Base](actions/get-knowledge-base.md) | GET | Retrieves knowledge base details from Famulor. |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET | Retrieves knowledge bases from Famulor. |
| [Update Knowledge Base](actions/update-knowledge-base.md) | PUT | Updates an existing knowledge base in Famulor. |

### Knowledge Base Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Knowledge Base Document](actions/get-knowledge-base-document.md) | GET | Retrieves document details from a Famulor knowledge base. |
| [List Knowledge Base Documents](actions/list-knowledge-base-documents.md) | GET | Retrieves documents from a Famulor knowledge base. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Available Languages](actions/retrieve-available-languages.md) | GET | Retrieves available assistant languages from Famulor. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Famulor. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from Famulor. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Famulor. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Famulor. |

### Llm Model

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Available Models](actions/retrieve-available-models.md) | GET | Retrieves available assistant AI models from Famulor. |

### Mid Call Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create Mid Call Tool](actions/create-mid-call-tool.md) | POST | Creates a new mid-call tool in Famulor. |
| [Delete Mid Call Tool](actions/delete-mid-call-tool.md) | DELETE | Deletes an existing mid-call tool from Famulor. |
| [Get Mid Call Tool](actions/get-mid-call-tool.md) | GET | Retrieves mid-call tool details from Famulor. |
| [List Mid Call Tools](actions/list-mid-call-tools.md) | GET | Retrieves mid-call tools from Famulor. |
| [Update Mid Call Tool](actions/update-mid-call-tool.md) | PUT | Updates an existing mid-call tool in Famulor. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Available Phone Numbers](actions/retrieve-available-phone-numbers.md) | GET | Retrieves available phone numbers from Famulor. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET | Retrieves the authenticated user's account details from Famulor. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Available Voices](actions/retrieve-available-voices.md) | GET | Retrieves available assistant voices from Famulor. |

