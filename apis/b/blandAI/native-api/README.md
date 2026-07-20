# Bland AI: Native API Reference

A consolidated summary of Bland AI's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.bland.ai/api-v1/post/calls
- **API base URL:** `https://api.bland.ai`

## Authentication

### API Key

Use a Bland AI API key in the authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.bland.ai/api-v1/get/me)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Account Details](actions/account-details.md) | `GET /v1/me` | [docs](https://docs.bland.ai/api-v1/get/me) |
| [Analyze Call With AI](actions/analyze-call-with-ai.md) | `POST /v1/calls/{call_id}/analyze` | [docs](https://docs.bland.ai/api-v1/post/calls-id-analyze) |
| [Call Details](actions/call-details.md) | `GET /v1/calls/{call_id}` | [docs](https://docs.bland.ai/api-v1/get/calls-id) |
| [Chat With Knowledge Base](actions/chat-with-knowledge-base.md) | `POST /v1/knowledge/chat` | [docs](https://docs.bland.ai/api-v1/post/knowledge-chat) |
| [Create Batch](actions/create-batch.md) | `POST /v2/batches/create` | [docs](https://docs.bland.ai/api-v1/post/batches) |
| [Create Citation Schema](actions/create-citation-schema.md) | `POST /v1/citation_schemas/` | [docs](https://docs.bland.ai/api-v1/post/citation-schemas) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /v1/knowledgebases` | [docs](https://docs.bland.ai/api-v1/post/vectors) |
| [Create Pathway](actions/create-pathway.md) | `POST /v1/pathway/create` | [docs](https://docs.bland.ai/api-v1/post/pathways) |
| [Create Pathway Version](actions/create-pathway-version.md) | `POST /v1/pathway/{pathway_id}/version` | [docs](https://docs.bland.ai/api-v1/post/create_pathway_version) |
| [Create Prompt](actions/create-prompt.md) | `POST /v1/prompts` | [docs](https://docs.bland.ai/api-v1/post/prompts) |
| [Discover Sitemap URLs](actions/discover-sitemap-urls.md) | `POST /v1/knowledge/crawl` | [docs](https://docs.bland.ai/api-v1/post/knowledge-crawl) |
| [Find Contact](actions/find-contact.md) | `POST /v1/contacts/find` | [docs](https://docs.bland.ai/api-v1/get/contacts-find) |
| [Get All Pathways Information](actions/get-all-pathways-information.md) | `GET /v1/pathway` | [docs](https://docs.bland.ai/api-v1/get/all_pathway) |
| [Get Batch](actions/get-batch.md) | `GET /v2/batches/{batch_id}` | [docs](https://docs.bland.ai/api-v1/get/batches-id) |
| [Get Citation Schema](actions/get-citation-schema.md) | `GET /v1/citation_schemas/` | [docs](https://docs.bland.ai/api-v1/get/citation-schemas-id) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/{contact_id}` | [docs](https://docs.bland.ai/api-v1/get/contacts-id) |
| [Get Corrected Transcripts](actions/get-corrected-transcripts.md) | `GET /v1/calls/{call_id}/correct` | [docs](https://docs.bland.ai/api-v1/get/calls-corrected-transcript) |
| [Get Knowledge Base](actions/get-knowledge-base.md) | `GET /v1/knowledge/{knowledge_base_id}` | [docs](https://docs.bland.ai/api-v1/get/knowledge-id) |
| [Get Single Pathway Information](actions/get-single-pathway-information.md) | `GET /v1/pathway/{pathway_id}` | [docs](https://docs.bland.ai/api-v1/get/pathway) |
| [List Batches](actions/list-batches.md) | `GET /v2/batches/list` | [docs](https://docs.bland.ai/api-v1/get/batches) |
| [List Calls](actions/list-calls.md) | `GET /v1/calls` | [docs](https://docs.bland.ai/api-v1/get/calls) |
| [List Citation Schemas](actions/list-citation-schemas.md) | `GET /v1/citation_schemas/list` | [docs](https://docs.bland.ai/api-v1/get/citation-schemas-list) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://docs.bland.ai/api-v1/get/contacts) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET /v1/knowledge` | [docs](https://docs.bland.ai/api-v1/get/knowledge) |
| [List Numbers](actions/list-numbers.md) | `GET /v1/inbound` | [docs](https://docs.bland.ai/api-v1/get/inbound) |
| [List Pathway Versions](actions/list-pathway-versions.md) | `GET /v1/pathway/{pathway_id}/versions` | [docs](https://docs.bland.ai/api-v1/get/pathway_versions) |
| [List Prompts](actions/list-prompts.md) | `GET /v1/prompts` | [docs](https://docs.bland.ai/api-v1/get/prompts) |
| [Number Details](actions/number-details.md) | `GET /v1/inbound/{phone_number}` | [docs](https://docs.bland.ai/api-v1/get/inbound-number) |
| [Prompt Details](actions/prompt-details.md) | `GET /v1/prompts/{prompt_id}` | [docs](https://docs.bland.ai/api-v1/get/prompts-id) |
| [Purchase Phone Number](actions/purchase-phone-number.md) | `POST /numbers/purchase` | [docs](https://docs.bland.ai/api-v1/post/inbound-purchase) |
| [Resolve Contact](actions/resolve-contact.md) | `POST /v1/contacts/resolve` | [docs](https://docs.bland.ai/api-v1/post/contacts-resolve) |
| [Scrape Websites](actions/scrape-websites.md) | `POST /v1/knowledge/learn` | [docs](https://docs.bland.ai/api-v1/post/knowledge-learn-web) |
| [Send Call](actions/send-call.md) | `POST /v1/calls` | [docs](https://docs.bland.ai/api-v1/post/calls) |
| [Send Call Using Pathways (Simple)](actions/send-call-using-pathways-simple.md) | `POST /v1/calls` | [docs](https://docs.bland.ai/api-v1/post/calls-simple-pathway) |
| [Send Call With Task (Simple)](actions/send-call-with-task-simple.md) | `POST /v1/calls` | [docs](https://docs.bland.ai/api-v1/post/calls-simple) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1/contacts/{contact_id}` | [docs](https://docs.bland.ai/api-v1/patch/contacts-id) |
| [Update Inbound Number Details](actions/update-inbound-number-details.md) | `POST /v1/inbound/{phone_number}` | [docs](https://docs.bland.ai/api-v1/post/inbound-number-update) |
| [Update Knowledge Base](actions/update-knowledge-base.md) | `PUT /v1/knowledge/{knowledge_base_id}` | [docs](https://docs.bland.ai/api-v1/put/knowledge-id) |
| [Update Pathway](actions/update-pathway.md) | `POST /v1/pathway/{pathway_id}` | [docs](https://docs.bland.ai/api-v1/post/update_pathways) |
| [Upload Text](actions/upload-text.md) | `POST /v1/knowledge/learn` | [docs](https://docs.bland.ai/api-v1/post/knowledge-learn-text) |
