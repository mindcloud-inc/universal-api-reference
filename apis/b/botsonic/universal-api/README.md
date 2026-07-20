# <img src="https://images.mindcloud.co/apps/icons/botsonic_1776872857222.png" alt="Botsonic logo" width="28" height="28"> Botsonic: Universal API

Botsonic is Writesonic's AI chatbot platform for generating bot responses and managing chatbot knowledge, conversations, FAQs, starter questions, and bots through REST APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botsonic/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://writesonic.com/botsonic
- **Vendor API docs:** https://docs.botsonic.com/docs/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List FAQs](actions/list-faqs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-faqs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST | Creates a new bot in Botsonic. |
| [Delete Bot](actions/delete-bot.md) | DELETE | Deletes an existing bot from Botsonic. |
| [Get Bot](actions/get-bot.md) | GET | Retrieves a specific bot from Botsonic. |
| [List Bots](actions/list-bots.md) | GET | Retrieves all bots in Botsonic. |

### Bot Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Bot API Key](actions/get-bot-api-key.md) | GET | Retrieves a bot API key from Botsonic. |

### Bot Data

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upload URLs](actions/bulk-upload-urls.md) | POST | Uploads multiple URLs as bot data in Botsonic. |
| [Delete Bot Data](actions/delete-bot-data.md) | DELETE | Deletes existing bot data from Botsonic. |
| [List Bot Data](actions/list-bot-data.md) | GET | Retrieves bot data from Botsonic. |

### Bot Data File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file as bot data in Botsonic. |

### Bot Data Text

| Action | Method | Description |
| --- | --- | --- |
| [Upload Text](actions/upload-text.md) | POST | Uploads text as bot data in Botsonic. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [End Chat](actions/end-chat.md) | PUT | Ends a chat conversation in Botsonic. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a specific conversation from Botsonic. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves all bot conversations from Botsonic. |

### Faq

| Action | Method | Description |
| --- | --- | --- |
| [Create FAQ](actions/create-faq.md) | POST | Creates a new FAQ in Botsonic. |
| [Delete FAQ](actions/delete-faq.md) | DELETE | Deletes an existing FAQ from Botsonic. |
| [List FAQs](actions/list-faqs.md) | GET | Retrieves all FAQs from a Botsonic bot. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Generate Business Response](actions/generate-business-response.md) | POST | Generates a business chatbot response in Botsonic. |
| [Generate Response](actions/generate-response.md) | POST | Generates a chatbot response in Botsonic. |

### Starter Preset

| Action | Method | Description |
| --- | --- | --- |
| [List Starter Presets](actions/list-starter-presets.md) | GET | Retrieves all starter presets from Botsonic. |

### Starter Question

| Action | Method | Description |
| --- | --- | --- |
| [Create Starter Question](actions/create-starter-question.md) | POST | Creates a new starter question in Botsonic. |
| [Delete Starter Question](actions/delete-starter-question.md) | DELETE | Deletes an existing starter question from Botsonic. |
| [List Starter Questions](actions/list-starter-questions.md) | GET | Retrieves all starter questions from Botsonic. |
| [Update Starter Question](actions/update-starter-question.md) | PUT | Updates an existing starter question in Botsonic. |

