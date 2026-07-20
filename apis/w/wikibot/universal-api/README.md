# <img src="https://images.mindcloud.co/apps/icons/logo-wikibot_1776462274429.png" alt="Wikibot logo" width="28" height="28"> Wikibot: Universal API

Wikibot provides AI agents for support and sales, with API actions for asking the bot questions, searching and managing its knowledge base, configuring webhooks, listing agents, and anonymizing or deanonymizing text.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wikibot/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wikibot.pro
- **Vendor API docs:** https://wikibot.pro/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Agents](actions/list-agents.md) | GET | Retrieves bot agents from Wikibot. |

### Anonymized Text

| Action | Method | Description |
| --- | --- | --- |
| [Anonymize Text](actions/anonymize-text.md) | POST | Anonymizes text in Wikibot. |

### Bot Answer

| Action | Method | Description |
| --- | --- | --- |
| [Ask Question](actions/ask-question.md) | POST | Creates a bot answer in Wikibot. |
| [Ask Question With Query Parameters](actions/ask-question-with-query-parameters.md) | GET | Retrieves a bot answer from Wikibot with query parameters. |

### Deanonymized Text

| Action | Method | Description |
| --- | --- | --- |
| [Deanonymize Text](actions/deanonymize-text.md) | POST | Deanonymizes text in Wikibot. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST | Creates a new knowledge base in Wikibot. |
| [Get Knowledge Base](actions/get-knowledge-base.md) | GET | Retrieves knowledge base details from Wikibot. |

### Knowledge Base Article

| Action | Method | Description |
| --- | --- | --- |
| [Search Knowledge Base](actions/search-knowledge-base.md) | GET | Finds knowledge base articles in Wikibot by search query. |

### Knowledge Base Document

| Action | Method | Description |
| --- | --- | --- |
| [Upload Knowledge Base Document](actions/upload-knowledge-base-document.md) | POST | Uploads a knowledge base document to Wikibot. |

### Webhook Url

| Action | Method | Description |
| --- | --- | --- |
| [Set Webhook URL](actions/set-webhook-url.md) | PUT | Updates the webhook URL in Wikibot. |

