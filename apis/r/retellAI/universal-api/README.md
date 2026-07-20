# <img src="https://images.mindcloud.co/apps/icons/retellai-logo_1773349833952.jpeg" alt="Retell AI logo" width="28" height="28"> Retell AI: Universal API

Manage AI voice agents, chats, calls, and phone numbers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/retellAI/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.retellai.com
- **Vendor API docs:** https://docs.retellai.com/api-references

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Voices](actions/list-voices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Phone Call](actions/create-phone-call.md) | POST | Creates a phone call in Retell AI. |
| [Create Web Call](actions/create-web-call.md) | POST | Creates a web call in Retell AI. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Retell AI. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from Retell AI. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | POST | Creates a chat in Retell AI. |
| [End Chat](actions/end-chat.md) | PUT | Ends an ongoing chat in Retell AI. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from Retell AI. |
| [List Chat](actions/list-chat.md) | GET | Retrieves chats from Retell AI. |

### Chat Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Agent](actions/create-chat-agent.md) | POST | Creates a chat agent in Retell AI. |
| [Get Chat Agent](actions/get-chat-agent.md) | GET | Retrieves a chat agent from Retell AI. |
| [List Chat Agents](actions/list-chat-agents.md) | GET | Retrieves chat agents from Retell AI. |
| [Publish Chat Agent](actions/publish-chat-agent.md) | PUT | Publishes a chat agent in Retell AI. |
| [Update Chat Agent](actions/update-chat-agent.md) | PUT | Updates a chat agent in Retell AI. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Add Knowledge Base Sources](actions/add-knowledge-base-sources.md) | PUT | Adds sources to a knowledge base in Retell AI. |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST | Creates a knowledge base in Retell AI. |
| [Get Knowledge Base](actions/get-knowledge-base.md) | GET | Retrieves a knowledge base from Retell AI. |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET | Retrieves knowledge bases from Retell AI. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone Number](actions/get-phone-number.md) | GET | Retrieves a phone number from Retell AI. |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers from Retell AI. |
| [Update Phone Number](actions/update-phone-number.md) | PUT | Updates a phone number in Retell AI. |

### Retell Llm

| Action | Method | Description |
| --- | --- | --- |
| [Create Retell LLM](actions/create-retell-llm.md) | POST | Creates a Retell LLM in Retell AI. |
| [Get Retell LLM](actions/get-retell-llm.md) | GET | Retrieves a Retell LLM from Retell AI. |
| [List Retell LLMs](actions/list-retell-llms.md) | GET | Retrieves Retell LLMs from Retell AI. |
| [Update Retell LLM](actions/update-retell-llm.md) | PUT | Updates a Retell LLM in Retell AI. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Voices](actions/list-voices.md) | GET | Retrieves voices from Retell AI. |

### Voice Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Voice Agent](actions/create-voice-agent.md) | POST | Creates a voice agent in Retell AI. |
| [Get Voice Agent](actions/get-voice-agent.md) | GET | Retrieves a voice agent from Retell AI. |
| [List Voice Agents](actions/list-voice-agents.md) | GET | Retrieves voice agents from Retell AI. |
| [Publish Agent](actions/publish-agent.md) | PUT | Publishes a voice agent in Retell AI. |
| [Update Voice Agent](actions/update-voice-agent.md) | PUT | Updates a voice agent in Retell AI. |

