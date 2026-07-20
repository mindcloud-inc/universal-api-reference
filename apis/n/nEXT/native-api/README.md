# NEXT: Native API Reference

A consolidated summary of NEXT's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.nextapp.co/
- **OpenAPI specification:** https://developer.nextapp.co/openapi.json
- **API base URL:** `https://rest.eu-west-1.nextapp.co/v1`

## Authentication

### API Key

Use the NEXT API token from Teamspace settings. NEXT requires the exact header Authorization: Token <apiKey>.

### Credentials

- **API Key:** `apiKey` · required · Your NEXT API token from Teamspace settings > Security & Privacy > API tokens.

[Official authentication documentation](https://developer.nextapp.co/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://developer.nextapp.co/) |
| [Create AI Prompt Template](actions/create-ai-prompt-template.md) | `POST /ai-prompt-templates` | [docs](https://developer.nextapp.co/) |
| [Create AI Query](actions/create-ai-query.md) | `POST /ai-queries` | [docs](https://developer.nextapp.co/) |
| [Create AI Rule](actions/create-ai-rule.md) | `POST /ai-rules` | [docs](https://developer.nextapp.co/) |
| [Create AI Thread](actions/create-ai-thread.md) | `POST /ai-threads` | [docs](https://developer.nextapp.co/) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://developer.nextapp.co/) |
| [Delete Account](actions/delete-account.md) | `DELETE /accounts/:id` | [docs](https://developer.nextapp.co/) |
| [Delete AI Prompt Template](actions/delete-ai-prompt-template.md) | `DELETE /ai-prompt-templates/:id` | [docs](https://developer.nextapp.co/) |
| [Delete AI Query](actions/delete-ai-query.md) | `DELETE /ai-queries/:id` | [docs](https://developer.nextapp.co/) |
| [Delete AI Rule](actions/delete-ai-rule.md) | `DELETE /ai-rules/:id` | [docs](https://developer.nextapp.co/) |
| [Delete AI Thread](actions/delete-ai-thread.md) | `DELETE /ai-threads/:id` | [docs](https://developer.nextapp.co/) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:id` | [docs](https://developer.nextapp.co/) |
| [Get Account](actions/get-account.md) | `GET /accounts/:id` | [docs](https://developer.nextapp.co/) |
| [Get AI Prompt Template](actions/get-ai-prompt-template.md) | `GET /ai-prompt-templates/:id` | [docs](https://developer.nextapp.co/) |
| [Get AI Query](actions/get-ai-query.md) | `GET /ai-queries/:id` | [docs](https://developer.nextapp.co/) |
| [Get AI Rule](actions/get-ai-rule.md) | `GET /ai-rules/:id` | [docs](https://developer.nextapp.co/) |
| [Get AI Thread](actions/get-ai-thread.md) | `GET /ai-threads/:id` | [docs](https://developer.nextapp.co/) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:id` | [docs](https://developer.nextapp.co/) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://developer.nextapp.co/) |
| [List AI Prompt Templates](actions/list-ai-prompt-templates.md) | `GET /ai-prompt-templates` | [docs](https://developer.nextapp.co/) |
| [List AI Rules](actions/list-ai-rules.md) | `GET /ai-rules` | [docs](https://developer.nextapp.co/) |
| [List AI Threads](actions/list-ai-threads.md) | `GET /ai-threads` | [docs](https://developer.nextapp.co/) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developer.nextapp.co/) |
| [Search Accounts](actions/search-accounts.md) | `GET /search-accounts` | [docs](https://developer.nextapp.co/) |
| [Update Account](actions/update-account.md) | `PUT /accounts/:id` | [docs](https://developer.nextapp.co/) |
| [Update AI Prompt Template](actions/update-ai-prompt-template.md) | `PUT /ai-prompt-templates/:id` | [docs](https://developer.nextapp.co/) |
| [Update AI Query](actions/update-ai-query.md) | `PUT /ai-queries/:id` | [docs](https://developer.nextapp.co/) |
| [Update AI Rule](actions/update-ai-rule.md) | `PUT /ai-rules/:id` | [docs](https://developer.nextapp.co/) |
| [Update AI Thread](actions/update-ai-thread.md) | `PUT /ai-threads/:id` | [docs](https://developer.nextapp.co/) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:id` | [docs](https://developer.nextapp.co/) |
