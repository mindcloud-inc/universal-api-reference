# <img src="https://images.mindcloud.co/apps/icons/f1ge6j4w-400x400_1773799717101.jpeg" alt="Bland AI logo" width="28" height="28"> Bland AI: Universal API

Manage Bland AI calls, prompts, pathways, and numbers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blandAI/latest
- **Category:** Communication / Video Communications
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bland.ai
- **Vendor API docs:** https://docs.bland.ai/api-v1/post/calls

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Account Details](actions/account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Account Details](actions/account-details.md) | GET | Retrieves account details from your Bland AI account. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch](actions/create-batch.md) | POST | Creates a new call batch in Bland AI. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves a batch from your Bland AI account. |
| [List Batches](actions/list-batches.md) | GET | Retrieves batches from your Bland AI account. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Call With AI](actions/analyze-call-with-ai.md) | GET | Retrieves AI analysis for a call in Bland AI. |
| [Call Details](actions/call-details.md) | GET | Retrieves call details from your Bland AI account. |
| [Get Corrected Transcripts](actions/get-corrected-transcripts.md) | GET | Retrieves corrected transcripts for a call in Bland AI. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from your Bland AI account. |
| [Send Call](actions/send-call.md) | POST | Creates a new call in Bland AI. |
| [Send Call Using Pathways (Simple)](actions/send-call-using-pathways-simple.md) | POST | Creates a pathway-based call in Bland AI. |
| [Send Call With Task (Simple)](actions/send-call-with-task-simple.md) | POST | Creates a task-based call in Bland AI. |

### Citation Schema

| Action | Method | Description |
| --- | --- | --- |
| [Create Citation Schema](actions/create-citation-schema.md) | POST | Creates a new citation schema in Bland AI. |
| [Get Citation Schema](actions/get-citation-schema.md) | GET |  |
| [List Citation Schemas](actions/list-citation-schemas.md) | GET | Retrieves citation schemas from your Bland AI account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Find Contact](actions/find-contact.md) | GET | Finds a contact in Bland AI. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from your Bland AI account. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Bland AI account. |
| [Resolve Contact](actions/resolve-contact.md) | POST | Finds or creates a contact in Bland AI. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Bland AI. |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Chat With Knowledge Base](actions/chat-with-knowledge-base.md) | GET | Chats with a knowledge base in Bland AI. |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST | Creates a new knowledge base in Bland AI. |
| [Discover Sitemap URLs](actions/discover-sitemap-urls.md) | GET | Retrieves sitemap URLs from a website in Bland AI. |
| [Get Knowledge Base](actions/get-knowledge-base.md) | GET | Retrieves a knowledge base from Bland AI. |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET | Retrieves knowledge bases from your Bland AI account. |
| [Scrape Websites](actions/scrape-websites.md) | POST | Scrapes websites into a knowledge base in Bland AI. |
| [Update Knowledge Base](actions/update-knowledge-base.md) | PUT | Updates an existing knowledge base in Bland AI. |
| [Upload Text](actions/upload-text.md) | POST | Uploads text to a knowledge base in Bland AI. |

### Pathway

| Action | Method | Description |
| --- | --- | --- |
| [Create Pathway](actions/create-pathway.md) | POST | Creates a new pathway in Bland AI. |
| [Get All Pathways Information](actions/get-all-pathways-information.md) | GET | Retrieves pathways from your Bland AI account. |
| [Get Single Pathway Information](actions/get-single-pathway-information.md) | GET | Retrieves a pathway from your Bland AI account. |
| [Update Pathway](actions/update-pathway.md) | PUT | Updates an existing pathway in Bland AI. |

### Pathway Version

| Action | Method | Description |
| --- | --- | --- |
| [Create Pathway Version](actions/create-pathway-version.md) | POST | Creates a new pathway version in Bland AI. |
| [List Pathway Versions](actions/list-pathway-versions.md) | GET | Retrieves pathway versions from Bland AI. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Numbers](actions/list-numbers.md) | GET | Retrieves inbound numbers from your Bland AI account. |
| [Number Details](actions/number-details.md) | GET | Retrieves inbound number details from Bland AI. |
| [Purchase Phone Number](actions/purchase-phone-number.md) | POST | Purchases a phone number in Bland AI. |
| [Update Inbound Number Details](actions/update-inbound-number-details.md) | PUT | Updates inbound number details in Bland AI. |

### Prompt

| Action | Method | Description |
| --- | --- | --- |
| [Create Prompt](actions/create-prompt.md) | POST | Creates a new prompt in Bland AI. |
| [List Prompts](actions/list-prompts.md) | GET | Retrieves prompts from your Bland AI account. |
| [Prompt Details](actions/prompt-details.md) | GET | Retrieves prompt details from your Bland AI account. |

